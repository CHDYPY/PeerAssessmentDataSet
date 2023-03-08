The peer assessment dataset was used in our paper, **SC-PA: A Spot-checking Model Based on Stackelberg Game Theory for Improving Peer Assessment**.

## Background and Source

It includes peer assessment data collected in real classroom environments from two practical teaching courses. Each homework assignment has a maximum score of 10 points, and each student will grade three submissions.

- **Experiment** **for the course "Data Structure" (Exp. 1)**: 207 students from three parallel classes participated in Exp. 1. In particular, the experiment group (EG) comprised 72 students from one of these classes who were asked to review their peers' submissions under the setting of our proposed SC-PA model. On the other hand, the control group (CG) consisted of 135 students from the remaining two classes who are required to evaluate their peers' submissions under the setting of the classical spot-checking model. 
- **Experiment for the course "Database Principles" (Exp. 2)**: There were 64 students from the same class taking part in the Exp. 2. Unlike Exp. 1, we organized eight peer assessment activities in Exp. 2, where the previous four activities are set with the SC-PA model, and the remaining half of the activities were associated with the classical spot-checking model. Under such circumstances, the first four peer assessment activities were deemed as the experiment group (EG), while the last four activities were treated as the control group (CG).

All data comes from our online peer assessment system database, and some sensitive information has been processed. The dataset contains approximately 3500 records. These datasets can provide support for some peer assessment techniques, such as score aggregation techniques. We welcome you to use this real dataset in your research and acknowledge the source of the dataset in your publication.

## Structure



The columns in this dataset are:

- HomeworkID
- GraderUserID
- GradeeUserID
- peerGrade
- teacherGrade

You can import this dataset in Python using the following code:

```python
import csv

def readFile(fileName, dataName):
    with open(fileName, encoding='UTF-8') as csvFile:
        reader = csv.reader(csvFile)
        for line in reader:
            dataName.append(line)
        del dataName[0]
        
data_experiment_1 = []
readFile('experimentGroup_1.csv', data_experiment_1)
```





