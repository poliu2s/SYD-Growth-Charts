# Rare Bone Growth Charts

A Growth Chart App for Children with Bone Dysplasias (‘The Door Frame Project’)

##What
Build a mobile app that allows patients with bone dysplasias to record their height and plot it on a growth chart appropriate for their condition.

##Why
A growth chart is a chart that shows the normal range for height at a given age (https://www.cdc.gov/growthcharts/). Plotting a child’s height on a growth chart is an easy way to monitor a child’s health. If a child’s height falls outside of the normal range, this could be an early warning sign that there is a serious medical problem.

Children with bone dysplasias have a genetic defect that prevents their bones from growing normally. The most common types of bone dysplasias are Achondroplasia, Pseudoachondroplasia, Diastrophic Dysplasia and Spondyloepiphyseal Dysplasia Congenita (SEDC). As these children grow differently from other children, they need to be plotted on growth charts specific to their condition. Since bone dysplasias are rare, it is difficult to collect sufficient measurements from lots of children with these conditions to produce a high quality growth chart. Low quality growth charts based on a small amount of measurements do exist (see PDFs below), but they are rarely used as many doctors are not aware of their existence. The goal of this project is therefore twofold: 1) promote the use of the existing growth charts and 2) collect height measurements from patients using the app to produce better growth charts in the future.

##What is the current solution to the problem?
Patients or doctors make photocopies of the disease specific growth charts and plot their patients on these (if they are aware they exist and can get their hands on these very old papers). 

##Solution
- Native iPhone and Android apps
Use growth charts from the publications provided
On first launch register new patient:
enter patient's name, sex, date of birth and diagnosis (dropdown for achondroplasia, pseudoachondroplasia, diastrophic dysplasia, SEDC)
Message: ‘the height measurements you are entering in this app will be used to produce better growth charts for your condition in the future. If you do not want your height measurements to be used this way, please tick the box below'
Message: 'to produce better growth charts for your condition in the future, it is important that we confirm your diagnosis and get some more details on your medical history. We would therefore like to contact you by email to ask you a few questions about your condition. Do you agree to be contacted by email?’ Tickbox ‘Yes, I agree to be contacted’ if ticked yes, enter email address
Option to register multiple patients and choose who is currently shown on the growth charts
Show growth chart for the active patient. Previously entered measurements are plotted on the growth chart as dots and connected with a line. Choose correct growth chart based on diagnosis and patient’s sex (if sex-specific growth charts are available)
‘+’ button to enter new measurement. Default to today’s date, but date can be changed by user (e.g. to record older measurements). Choose unit of measure (cm of feet/inches) in preferences.
option to add a comment to each measurement (for example to record that patient was sick at the time of measurements, or other factors that might influence the accuracy of the measurement).
Option to export the growth chart with recorded measurements as a PDF (e.g. to put into medical records)
Store entered measurements on a server: use unique ID assigned by app to identify individual patient without using their name. Also need to store patient’s sex, date of birth, diagnosis, email address (if given).
A way to push updated growth charts back to user (e.g. through App update?)

- We also decided to leverage Apple's ResearchKit in order to provide a seemless survey on Apple's iOS platform. This iOS app that we created is primarily targeted towards clinicians and researchers who can fill out the metrics described above but during a one-off event without the need to create profiles. We hope that this app can provide an additional source of data onto which we can start building the largest repository of rare bone diseases.
