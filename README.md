# Exp_05: Risk-assessment
### Name:Thilakeswaran KP
### Reg No: 212223230232
## AUDITING CLOUD ACTIVITY USING AWS CLOUDTRAIL

## Objective

To audit and monitor cloud activity in AWS using **AWS CloudTrail** by viewing and analyzing recorded AWS events and identifying important audit information such as user identity, event name, event time, AWS service, region, and operation status.

## Requirements

AWS Account

Web Browser

Internet Connection

Amazon S3 access

AWS CloudTrail

**PART A — ACCESS AWS CLOUDTRAIL**

**Step 1: Login to AWS**

1. Open the **AWS Management Console**.

2. Sign in using your AWS account.

3. In the AWS search bar, type **CloudTrail**.

4. Select **AWS CloudTrail**.

<img width="1912" height="922" alt="image" src="https://github.com/user-attachments/assets/78fb7259-bb84-4f3b-9813-fb4922b9823f" />

**Step 2: Open Event History**

1. In the CloudTrail navigation menu, select **Event history**.

2. CloudTrail displays recent AWS activity.

3. Review the available events.

The Event History page may display information such as:

Event time

Username

Event name

Event source

Resource type

Resource name
<img width="1910" height="803" alt="image" src="https://github.com/user-attachments/assets/5b2a80d1-1c69-48c1-88d7-1f489ece56e1" />

**PART B — ANALYZE A CLOUDTRAIL EVENT**

**Step 3: Select an Event**

1. From the Event History list, select an S3-related event.

2. Click the event to open its details.

3. Examine the event information and the event record/JSON.

For this experiment, a **CreateBucket** event can be used.

**Step 4: Analyze the CreateBucket Event**

The CreateBucket event indicates that an **Amazon S3 bucket creation operation** occurred.

Record the following information:

| Parameter | Observation |
|---|---|
| Event Time | August 05, 2026, 11:07:59 (UTC+05:30) |
| User Name | root |
| Event Name | CreateBucket |
| Event Source | s3.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | false |
| Error Code | - |
| Activity | S3 bucket creation |

**Meaning of Important Fields**

| Field | Meaning |
|---|---|
| **Event Time** | Time at which the activity occurred |
| **User Name** | User/identity associated with the activity |
| **Event Name** | AWS operation that was performed |
| **Event Source** | AWS service that generated the event |
| **AWS Region** | Region where the activity occurred |
| **Read-only** | Indicates whether the event was only a read operation or involved a change |
| **Error Code** | Indicates whether an error occurred |

<img width="1907" height="906" alt="image" src="https://github.com/user-attachments/assets/2a44b5a5-1ee3-478c-8a27-4c900cb8c4cf" />

**PART C — IDENTIFY ANOTHER CLOUDTRAIL EVENT**

**Step 5: Select Another Event**

1. Return to **CloudTrail → Event history**.

2. Select another event.

3. Open its details.

4. Record the important fields.

For example, an event such as:

**AutomatedDefaultVpcCreation**

may be present.

This event is associated with **Amazon EC2**.

**Step 6: Analyze the Second Event**

Record:

| Parameter | Observation |
|---|---|
| Event Time | August 27, 2026, 09:27:38 (UTC+05:30) |
| User Name | - |
| Event Name | AutomatedDefaultVpcCreation |
| Event Source | ec2.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | false |
| Error Code | - |
| Activity | Automated default VPC creation |

<img width="1901" height="917" alt="image" src="https://github.com/user-attachments/assets/71c81180-d322-43b8-9a5b-89200552dcc0" />

**PART D — COMPARE THE EVENTS**

**Step 7: Prepare the Audit Comparison**

Compare the two CloudTrail events.

| Parameter | Event 1 | Event 2 |
|---|---|---|
| Event Time | August 05, 2026, 11:07:59 (UTC+05:30) | August 27, 2026, 09:27:38 (UTC+05:30) |
| User Name | root | - |
| Event Name | CreateBucket | AutomatedDefaultVpcCreation |
| Event Source | s3.amazonaws.com | ec2.amazonaws.com |
| AWS Region | us-east-1 | us-east-1 |
| Read-only | false | false |
| Error Code | - | - |
| Activity | S3 bucket creation | Automated VPC creation |

**PART E — SECURITY AUDIT ANALYSIS**

**Step 8: Identify Who, What, When and Where**

For each event, identify:

**WHO?**

Who or which identity performed/generated the activity?

**WHAT?**

What AWS operation was performed?

**WHEN?**

At what date and time did the activity occur?

**WHERE?**

In which AWS Region did the activity occur?

**RESULT?**

Was the operation successful or did it generate an error?

**Step 9: Prepare the Final Audit Table**

Students should prepare a final table similar to the following:

| Event Time | User Name | Event Name | Service | Region | Read-only | Result | Activity |
|---|---|---|---|---|---|---|---|
| August 05, 2026, 11:07:59 (UTC+05:30) | root | CreateBucket | Amazon S3 | us-east-1 | false | Operation Successful | S3 bucket creation |
| August 27, 2026, 09:27:38 (UTC+05:30) | - | AutomatedDefaultVpcCreation | Amazon EC2 | us-east-1 | false | Operation Successful | Automated VPC creation |

**PART F — SCREENSHOTS TO SUBMIT**

Students should capture the following screenshots:

1. **AWS CloudTrail Dashboard**
<img width="1912" height="922" alt="image" src="https://github.com/user-attachments/assets/e0a5a6b0-19f0-492f-b376-6ca35e28445d" />

2. **CloudTrail Event History**
<img width="1910" height="803" alt="image" src="https://github.com/user-attachments/assets/ae6b6cbf-0fda-4e19-88cd-df08e9a9f88b" />

3. **CreateBucket Event Details**
<img width="1907" height="906" alt="image" src="https://github.com/user-attachments/assets/7e3d9af6-77dc-471e-97fb-2a53bb64a488" />

4. **Second CloudTrail Event Details**
<img width="1901" height="917" alt="image" src="https://github.com/user-attachments/assets/71c81180-d322-43b8-9a5b-89200552dcc0" />

5. **Final Audit/Observation Table**

## RESULT

**The cloud activities in AWS were successfully audited using AWS CloudTrail Event History. Different AWS events were examined based on event time, user identity, event name, event source, AWS Region, read-only status, and error status. The experiment demonstrated how AWS CloudTrail provides an audit trail for monitoring, accountability, and investigation of cloud activities.**

