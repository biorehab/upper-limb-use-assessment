# Upper Limb Use Assessment

This is a repository of jupyter notebooks and python scripts used for analyzing upper limb use measures.

The code was developed for executing it in Google Colab. So, to test this code, you will need to download the repository, and upload it into your Google Drive. Once uploaded, you should be able to run the Python notebooks files using Google Colab. The data generated from the notebooks are saved on Google Drive.

There is a variable that needs to be modified in each notebook when you want to execute the code from your Google Drive. This is explained in the individual notebooks.

## Notebooks in the repository
There are two notebooks in this repository:


[**results.ipynb**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/notebooks/results.ipynb)

Generates results from paper on upper limb use assessments.

[**generate_classifier_outputs.ipynb**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/notebooks/generate_classifier_outputs.ipynb)

Generates and saves binary outputs using different upper limb use measures.

## Data
There are four data files in this repository:

[**right.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/right.csv)

Contains data from the right arm of the control subjects.

[**left.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/left.csv)

Contains data from the left arm of the control subjects.

[**unaffected.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/unaffected.csv)

Contains data from the unaffected arm of the patients.

[**affected.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/affected.csv)

Contains data from the affected arm of the patients.

The columns in each of the four files are, 
time, subject, ax, ay, az, gx, gy, gz, r1, r2, g1, g2, yaw, pitch, task, use_type

There were 10 controls and 5 patients in the study.

Columns ax, ay, and az correspond to data from the 3 axes of the accelerometer and gx, gy, and gz correspond to data from the 3 axes of the gyroscope data. The sensor data was recorded at 50 Hz.

The experiment videos were annotated using the FAABOS scale by 2 therapists twice with a week between each annotation. Columns r1 and r2 correspond to  first and second annotations made by one therapist, and g1 and g2 correspond to those by the other therapist. Video annotations were saved at 30 Hz and are up-sampled here to match the sensor data frequency.

Yaw and pitch angles were calculated from the accelerometer and gyroscope data using the Madgwick algorithm.

The task column contains strings corresponding to what task was performed at that instant (eg. ‘ButtonShirt’ or ‘Walk25’). The use_type column has ‘Arm’, ‘Hand’ or ‘NF’ corresponding to tasks that make use of primarily arms or primarily hands, or non-functional tasks respectively.
