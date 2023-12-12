# Analyze-live-streaming-data-using-ThingsBoard

## 


1.	Navigate to Firebase. In the module24Project Realtime database, create a new field titled alarms and initialize the corresponding field to zero.
Provide a screenshot to show that you created the alarm field inside your Realtime database and initialized it to zero.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/55ba7817-11de-4cda-a259-245453cd0a01">

2.	Navigate to the ThingsBoard home page. Create a new rule chain titled “CreateAndClearAlarms” by following the steps shown in Mini-Lesson 24.5.
Provide a screenshot to show that you created the CreateAndClearAlarms rule chain with all of the necessary components.

<img width="459" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/ccae0d30-feaa-4d24-b5de-5c15446e0474">

3.	Create another rule chain and name it “TempToFirebase”.
Provide a screenshot to show that you created the TempToFirebase rule chain with all of the necessary components.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/bee86970-ab70-4511-a66c-6d174cd9166f">

4.	Open the TempToFirebase rule chain. Add a “rest API call” node and name it “TempToFirebase”. Replace the default link with the following link:
https://module24project-default-rtdb.firebaseio.com/temperature.json
Select “Add” to add the TempToFirebase node to your Rule Engine. Connect the Input and TempToFirebase nodes.
Provide two screenshots. The first screenshot should show that you added the TempToFirebase node to your Rule Engine correctly. The second screenshot should show that you connected the Input and TempToFirebase nodes.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/832d9414-93e4-45b9-a1de-e49586788121">

<img width="539" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/6fcfe1b8-abf9-46cd-8322-71f2fed417d7">

5.	Create another rule chain and name it “AlarmToFirebase”.
Provide a screenshot to show that you created the AlarmToFirebase rule chain with all of the necessary components.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/fd542c64-12e4-44e9-b25d-f794ed034a9c">

6.	Open the AlarmToFirebase rule chain. Add a “rest API call” node and name it “AlarmToFirebase”. Replace the default link with the following link:
https://module24project-default-rtdb.firebaseio.com/alarm.json
Select “Add” to add the AlarmToFirebase node to your Rule Engine. Connect the Input and AlarmToFirebase nodes.
Provide two screenshots. The first screenshot should show that you added the AlarmToFirebase node to your Rule Engine correctly. The second screenshot should show that you connected the Input and AlarmToFirebase nodes.
 
<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/c0549722-da3c-46e0-af78-43ab8f9dcf55">

<img width="468" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/a70ce35f-3f2f-403d-b798-0007d559c53a">

7.	Open the CreateAndClearAlarms rule chain that you created in Step 2. Add a “rule chain” node. Title this node “AlarmToFirebase” and select AlarmToFirebase as the rule chain. Select “Add” to add the AlarmToFirebase node to your Rule Engine.
Provide a screenshot to show that you added the AlarmToFirebase node to your Rule Engine correctly.

<img width="481" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/4dbdbce3-6e35-4ce0-9a03-1e25299b7c55">

8.	Connect the CreateAlarm and AlarmToFirebase nodes. Add “Created” as the link label.
Provide a screenshot to show that you connected the CreateAlarm and AlarmToFirebase nodes with a Created link label.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/03f39426-7537-4ed3-8d6f-c7221a2ba297">

9.	Add another “rule chain” node to the CreateAndClearAlarms rule chain. Title this node “TempToFirebase” and select TempToFirebase as the rule chain. Select “Add” to add the TempToFirebase node to your Rule Engine.
Provide a screenshot to show that you added the TempToFirebase node to your Rule Engine correctly.

<img width="458" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/dbd106d2-4012-4772-a162-762f1ffd1304">

10.	Connect the MaxTemp and TempToFirebase nodes. Add “True” as the link label.
Provide a screenshot to show that you connected the MaxTemp and AlarmToFirebase nodes with a True link label.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/e35f16ec-cb6e-4cff-afb3-4b5896d991bc">

11.	Open the Root Rule Chain in ThingsBoard. Add a “rule chain” node. Name it “CreateAndClearAlarm” and select CreateAndClearAlarm as the rule chain. Select “Add” to add the CreateAndClearAlarm node to your Rule Engine.
Provide a screenshot to show that you added the CreateAndClearAlarm node to your Rule Engine correctly.

<img width="493" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/1f6d1782-3b55-4bf6-a801-4f918f252074">

12.	Connect the SaveTimeseries and CreateAndClearAlarm nodes. Add “Success” as the link label.
Provide a screenshot to show that you connected the SaveTimeseries and CreateAndClearAlarm nodes with a Success link label.

<img width="563" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/bf059286-8a66-4f77-9512-e5459dc9053c">

13.	Navigate to Firebase and open the alarm and temperature fields.
Provide two screenshots. The first screenshot should show that the alarm field is being populated with the live streaming data from the CreateAndClearAlarm rule chain. The second screenshot should show that the temperature field is being populated with temperature and humidity data.
 
<img width="504" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/62483245-2b95-47d0-9f56-06f9918915c5">

<img width="331" alt="image" src="https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/458a1f00-9d05-44a2-9e70-4483aecc1275">

![image](https://github.com/sandip86/Analyze-live-streaming-data-using-ThingsBoard/assets/153111110/3f2b02ce-7e48-4f74-bf4c-58ce4293f53c)
