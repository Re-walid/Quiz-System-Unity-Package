## Creating Quiz Data

Right-click in your desired folder then go to:

- **Create \> Quiz System \> Data**

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/5e82abfd-ae9f-4084-a919-bea80f7163be)

> To tailor your Quiz data to suit your specific needs and requirements,
> the following steps will guide you through the customization process:

1. **Adding Questions:**

    -   Begin by populating the Questions List with Question elements.

    -   For each question, determine the Question Type:

        -   Text Type: Specify the question by entering a string in the
            \"Question Text\" field.

        -   Image Type: Attach an image to the question by selecting a
            Sprite in the \"Question Image\" field.

2.  **Adding Answers:**

    -   Select the appropriate Answer Type for each question:

        -   Text Type: Enables you to input text as the answer.

        -   Image Type: Enables you to select an image as the answer.

    -   Populate the Answers List with Answer elements.

      ![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/fc249f9f-0f2e-442a-b69b-753ebe8e81a9)

    -   Specify the correct answer by checking the Is Correct checkbox.

3.  **Adding Time:**

    -   Specify whether your question has timer by checking the Has Time
        checkbox.

        -   Question Timer Data will appear for you, you can specify the
            Timer Type Seconds or (Minutes, Hours) the last two are not
            supported in this version. And the Timer Value.

            ![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/5629e499-69e0-4fcd-8d01-04ba573a4c57)


> By following these steps, you can easily customize your Quiz data,
> allowing for a seamless integration into your project while meeting your
> specific requirements.

-   Drag and Drop the Quiz System Handler from: Quiz System \> Prefabs,
    Into your scene.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/53d73509-2648-4bb5-a555-207aea53cc1b)


You have the option to specify the Quiz Load Mode according to your
preferences. There are three available modes to choose from:

-   **Instantiate Mode:**

    -   Selecting this mode will instantiate the Quiz Prefab and Quiz
        Result Prefab during runtime.

    -   This means that the Quiz and Quiz Result objects will be created
        dynamically when needed.

-   **Include Mode:**

    -   Choosing this mode will include the Quiz Prefab and Quiz Result
        as part of your scene.

    -   These objects will be automatically added to your scene when you
        select this mode.

-   **New Scene Mode:**

    -   Opting for this mode will open a separate Quiz scene.

    -   You can specify the scene load mode as either Additive or
        Single.

> Please consider the following details when choosing the scene load
> mode:

-   **Additive Load Mode:**

    -   If you select this mode, the Quiz scene will be loaded alongside
        your existing scene(s).

    -   This allows you to combine the Quiz functionality with your
        current scene setup.

-   **Single Load Mode:**

    -   By choosing this mode, only the Quiz scene will be loaded,
        replacing any existing scene(s).

    -   This is useful if you want to focus solely on the Quiz without
        any distractions from other scenes.

-   **Quiz Scene**:

    -   The Quiz Scene serves as an example scene that is preconfigured
        with all the necessary elements for the Quiz System.

    -   You can modify this scene according to your specific
        requirements,and you can include another Scene if desired.

    -   It is important to ensure that the Quiz Scene reference is never
        null if you intend to use the Quiz Load Mode: New Scene.

-   **Quiz Prefab**:

    -   The Quiz Prefab is an object that contains the Quiz System
        Manager script and all the essential UI elements required for
        the Quiz System to function properly.

    -   This prefab is ready to be used and can be customized as per
        your preferences.

-   **Quiz Result Prefab**:

    -   The Quiz Result Prefab represents the result panel that is
        displayed after completing the quiz.

    -   It is not mandatory to include this prefab, and you have the
        option to delete it if you prefer not to have a result panel.

    -   Alternatively, you can create your own custom result script,
        ensuring that it inherits from the QuizResultUI Class.

-   **Quiz Data Ref**:

    -   Quiz Data Ref is a Scriptable Object that contains a QuizData
        variable.

    -   This Scriptable Object is used to hold a reference to the
        QuizData across multiple scripts, allowing for modular and
        reusable code.

    -   By utilizing this reference, scripts can access the QuizData
        without creating tight dependencies between them.

-   **Current Quiz Manager & Current Quiz Result Panel**:

    -   If you choose the Quiz Load Mode to be either Include or
        Instantiate, these variables will hold references to the Quiz
        Manager and Quiz Result objects within your scene.

    -   However, in the New Scene Mode, these variables will be null as
        the Quiz Manager and Quiz Result are not instantiated and exist
        in another scene.

-   **Open Quiz Automatically**:

    -   Open Quiz Automatically is another Scriptable Object that
        contains a boolean variable.

    -   This variable determines whether the Quiz System should open
        automatically or require manual activation.

    -   Based on the value of this variable, you can configure the
        behavior of the Quiz System.

```{=html}
<!-- -->
```

## Opening The Quiz System:

There are multiple ways to open the Quiz System, allowing you to select
the method that best suits your requirements. One of these methods is
the \"Manual\" approach:

-   **Manual**:

    -   To open the Quiz System manually, you can add the Quiz Opener
        Manual script to the desired object in your scene.

    -   This script allows you to trigger the opening of the Quiz System
        at your discretion.

    -   Remember to reference your Quiz Data within the script to ensure
        that the appropriate quiz content is loaded.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/c3e67e84-8de5-406a-b8e4-131755937214)


-   Now you can drag and drop this component into a custom event and
    choose QuizOpenerManual -\> Open() method like this.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/72a5bcf7-006d-48b0-a485-032bb46ac437)


-   You can do this with the OnClick event on the UI Button component:

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/b9f59187-25b5-42d0-87ad-01837a2ab54f)


-   **Automatically**:

    -   **UI**:

        -   To automatically open the Quiz System through a UI element,
            you can add the Quiz Opener Auto UI script to the desired
            object in your scene.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/c35559dc-044c-4ec0-b144-0cb5b118bdf1)


-   **2D / 3D Colliders**:

    -   If you want to trigger the Quiz System through collision with a
        2D or 3D collider, you can add the Quiz Opener Auto Collider
        script to the desired object in your scene.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/7d1cacbc-6456-4051-8045-e4ac8ed97050)


-   Make sure to reference your Quiz Data within the script to ensure
    the correct quiz content is loaded.

And That's all you need, the Quiz System will open when ever you click
on a UI or a Collider.

```{=html}
<!-- -->
```

## Quiz Result Data:

The Quiz Result data is Scriptable Object, It includes essential
information such as:

-   Total Number of Questions.

-   Number of Correct Answers.

-   Number of Incorrect Answers.

-   The percentage of correct Answers.

-   Time Taken to finish the Quiz.

![image](https://github.com/Re-walid/Quiz-System-Unity-Package/assets/46139244/bbe6cce2-149b-4002-aa24-74b088fe814c)

-   Leverage this data to gain valuable insights.
-   You can create custom scripts and reference this Scriptable Objects
    to make informed decisions in your Gameplay.
