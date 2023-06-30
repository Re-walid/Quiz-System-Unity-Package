# Quiz-System-Unity-Package
•	Create > Quiz System > Data

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/bcd2ffae-2cbd-40e2-9f23-570ab3e47777)

To tailor your Quiz data to suit your specific needs and requirements, the following steps will guide you through the customization process:

1.	Adding Questions:

	•	Begin by populating the Questions List with Question elements.

	•	For each question, determine the Question Type:

			o	Text Type:  Specify the question by entering a string in the "Question Text" field.
			o	Image Type:  Attach an image to the question by selecting a Sprite in the "Question Image" field.

2.	Adding Answers:

	•	Select the appropriate Answer Type for each question:

			o	Text Type: Enables you to input text as the answer.
			o	Image Type: Enables you to select an image as the answer.

	•	Populate the Answers List with Answer elements.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/b4cfdab2-24e1-4200-ad03-e769c6c4f8f0)

	•	Specify the correct answer by checking the Is Correct checkbox.

	•	Include Mode:

			o	Choosing this mode will include the Quiz Prefab and Quiz Result as part of your scene.
			o	These objects will be automatically added to your scene when you select this mode.

• New Scene Mode:

			o	Opting for this mode will open a separate Quiz scene.
			o	You can specify the scene load mode as either Additive or Single.

 Please consider the following details when choosing the scene load mode:

			o	Additive Load Mode:

					If you select this mode, the Quiz scene will be loaded alongside your existing scene(s).
					This allows you to combine the Quiz functionality with your current scene setup.

			o	Single Load Mode:

					By choosing this mode, only the Quiz scene will be loaded, replacing any existing scene(s).
					This is useful if you want to focus solely on the Quiz without any distractions from other scenes.


•	Quiz Scene: 
o	The Quiz Scene serves as an example scene that is preconfigured with all the necessary elements for the Quiz System.
o	You can modify this scene according to your specific requirements,and you can include another Scene if desired.
o	It is important to ensure that the Quiz Scene reference is never null if you intend to use the Quiz Load Mode: New Scene.
•	Quiz Prefab: 
o	The Quiz Prefab is an object that contains the Quiz System Manager script and all the essential UI elements required for the Quiz System to function properly.
o	This prefab is ready to be used and can be customized as per your preferences.
•	Quiz Result Prefab: 
o	The Quiz Result Prefab represents the result panel that is displayed after completing the quiz.
o	It is not mandatory to include this prefab, and you have the option to delete it if you prefer not to have a result panel.
o	Alternatively, you can create your own custom result script, ensuring that it inherits from the QuizResultUI Class.
