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

[**right.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/data/right.csv)

Contains data from the right arm of the control subjects.

[**left.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/control/data/left.csv)

Contains data from the left arm of the control subjects.

[**unaffected.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/patient/data/unaffected.csv)

Contains data from the unaffected arm of the patients.

[**affected.csv**](https://github.com/biorehab/upper-limb-use-assessment/blob/master/patient/data/affected.csv)

Contains data from the affected arm of the patients.

The columns in each of the four files are, 
time, ax, ay, az, gx, gy, gz, pitch, yaw, mx, my, mz, subject, old_time, r1, r2, g1, g2, task, use_type, gnd

### Subjects

There were 10 controls and 5 patients in the study. The subject column contains numbers unique to each subject.

### Time 

The column 'old_time' contains time on the watch while recording. Delay (~1s) between the video and the watches was corrected by observing the data and video simultaneously. Corrected time is included in the time column.

### Sensor data

Columns ax, ay, and az correspond to data from the 3 axes of the accelerometer, gx, gy, and gz correspond to data from the gyroscope and mx, my, and mz correspond to data from the magnetometer. The sensor data were recorded at 50 Hz.

Yaw and pitch angles were calculated from the accelerometer and gyroscope data using the Madgwick algorithm.

### Video annotations

The experiment videos were annotated using the FAABOS scale by 2 therapists twice with a week between each annotation. Columns r1 and r2 correspond to  first and second annotations made by one therapist, and g1 and g2 correspond to those by the other therapist. The gnd column corresponds to final ground truth used for analysis. It was obtained by taking the majority of r1, r2, g1, and g2, a label was chosen randomly in the event of a tie. Video annotations were saved at 30 Hz and are up-sampled here to match the sensor data frequency.

The task column contains strings corresponding to what task was performed at that instant (eg. ‘ButtonShirt’ or ‘Walk25’). The use_type column has ‘Arm’, ‘Hand’ or ‘NF’ corresponding to tasks that make use of primarily arms or primarily hands, or non-functional tasks respectively.

## Publications

David, A., ReethaJanetSureka, S., Gayathri, S., Annamalai, S. J., Samuelkamleshkumar, S., Kuruvilla, A., Magimairaj, H. P., Varadhan, S., & Balasubramanian, S. (2021). [**Quantification of the relative arm use in patients with hemiparesis using inertial measurement units**](https://journals.sagepub.com/doi/full/10.1177/20556683211019694). Journal of Rehabilitation and Assistive Technologies Engineering.

Subash, T., David, A., ReetaJanetSurekha, S., Gayathri, S., Samuelkamaleshkumar, S., Magimairaj, H. P., ... & Balasubramanian, S. (2022). [**Comparing algorithms for assessing upper limb use with inertial measurement units**](https://www.biorxiv.org/content/10.1101/2022.02.24.481756v1.full). bioRxiv.

