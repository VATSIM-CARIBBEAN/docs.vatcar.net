---
label: "Exam Center"
icon: book
order: 100
---

# Exam Center

This is the main exam management center. You will be able to create, edit, and delete exams as well as view exam statistics for your division.

!!!warning
Exam Statistics is currently unavailable.
!!!

## Assign Exam

You are able to assign any of your published exams to a controller by navigating to the assign exam button. This will automatically send the controller the exam and you will not have to do anything further.

## Pending Exams

You will be able to see all pending exams that have been assigned to students. From here, you are able to delete the exam.

Below the current pending exams, you are able to see exams that are waiting to be reassigned. When a student fails an exam, if there is a set automatic reassignment, it will show up here. Instructors are able to reassign the exam earlier than the reassign date, though it is not recommended to do so.

## Manage Exams

This is where the training administrator can manage their facility exams. You can create a new exam or edit existing exams. We will go through how to create and edit an exam.

!!!danger Warning
You will be unable to delete an exam after creating one. If you wish for it to be deleted, contact VATCAR3 with an explanation.
!!!

### Creating an Exam

When creating an exam, you have the ability to determine what percentage the member needs to pass the exam. You also have the ability to determine the retake period, how long a member can retake the exam after failing it. By default, this is set to 3.

### Editing an Exam

On the edit page, you are able to edit more options with the exam. This is also where you can add questions to your exam.

#### Exam Options

1. Exam Name
    - This is where you can put the name of your exam. Your facility's short code will be put before the name automatically.
2. Exam Status
    - If you are currently working on the exam, you can set the status to draft.
    - If the exam is ready to be deployed, you can set the status to active.
    - If you are retiring the exam and no longer wish to deploy it, you can set the status to Disabled/Retired.
3. Passing Percentage
    - This is the percentage a student needs to obtain on the exam in order to pass it. By default, this is set to 80%.
4. Required CBT (optional)
    - If you want a student to complete a computer based training module prior to taking an exam, you can specify the block here. If set to none, this exam will not need any module completed to be able to take this exam.
    - This does not automatically assign a user the exam after they complete the CBT.
5. Retake Days
    - This is the number of days the student has to wait prior to retaking the exam if they failed it. By default, this is set to 3 days.
6. Questions to Ask
    - If you wish to ask only a certain number of questions, you can put the number here. The test will take a set of random questions from the question bank and assign it to the user.
    - If you wish to ask all the questions, set the value to 0.
    - If the student retakes the exam, it will randomly select the questions again.
7. Premature Exam Results
    - This lets the student see the results of their exams as they are completing it. This will let them see the correct answer too.
    - This should generally be set to disabled for most facility exams.
8. Exam Type
    - You can se the type of exam here. By default, this should be set to FIR Exam.

#### Modifying Questions

Here, you can modify, edit, or add questions to your exam. To begin, you would create a question with the question itself, the type, and if the question is required. If the question type is True/False, you can select the correct answer there. If the question type is multiple choice, you will have to edit the question after creating it to add options.

!!!info
If the exam selects a group of random questions, the required option will force the exam to add those questions in every time.
!!!

After creating the question, you can begin editing it. When you navigate to the edit menu, you have the following options:

1. Edit Question
    - This is where you can edit your question to be asked.
2. Exam Image
    - If your question requires referencing an image, you can attach an image here. This is optional.
3. Question Required
    - If set the true and the exam pulls a random number of questions, this question will always be asked on the exam.

If your question is a multiple choice question, you have the option to create the choices and edit them below. You will want to begin by adding an option and determining whether the option is the correct answer or not. After you create multiple options, if you wish to change what the correct answer is, you can click on the check mark associated with the option. There can only be one correct answer. You also have the ability to delete the options.

!!!warning
You are unable to rename options, you will have to delete and remake.
!!!

## Exam Statistics

This page is currently unavailable. When released, this portion of the documentation will be updated.