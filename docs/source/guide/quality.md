---
title: Review annotations in Label Studio
type: guide
order: 404
meta_title: 
meta_description:
---

> Beta documentation: Label Studio Enterprise v2.0.0 is currently in Beta. As a result, this documentation might not reflect the current functionality of the product.

After multiple labelers have annotated tasks, review their output to validate the quality of the results. You can also perform this task after a model has predicted labels for tasks in your dataset. 

> The annotation review workflow is only available in Label Studio Enterprise Edition. If you're using Label Studio Community Edition, see [Features of Label Studio](label_studio_compare.html) to learn more.

## Why review annotations?

Data labeling is a crucial step for training many machine learning models, and it's essential to review annotations to make sure that only the highest quality data is used to train your machine learning model. If you don't review the quality of labeled data, weak annotations might be used when training your model and degrade overall model performance. READ MORE IN THIS BLOG POST???

## Choose what to review

You can start reviewing tasks randomly, or order tasks in the project data manager in different ways, depending on your use case:
- Order tasks by annotator, to review annotations and assess individual annotator performance at the same time.
- Order tasks by consensus score, to review annotations with more uncertainty first. 
- Order tasks by model confidence score, to review the annotations that a machine learning model was less certain about first. 

## Review annotated tasks

After you choose what to review, start reviewing annotated tasks:
1. From within a project, click the blue **Review Tasks** button. If you select a subset of tasks to review, the number of those tasks appears in the button.
2. Review the first task and annotation. By default, you view the tasks in numeric order. You can see the annotator and their annotation. 
- If the annotation is correct, click **Accept**.
- If the annotation is mostly correct, you can correct it by selecting a different option, changing which region is selected, moving the bounding box, or whichever makes sense for the type of labeling you're reviewing. After correcting the annotation, click **Fix & Accept**. 
- If the annotation is completely incorrect, or you don't want to attempt to correct it at all, click **Reject** to reject the annotation.
3. Continue reviewing annotated tasks until you've reviewed all annotated tasks. Click **Data Manager** to return to the list of tasks for the project. 



To place the task back in the Label Stream for annotation, you must delete the annotation (Rejecting the current one doesn't seem to do that?)


If there are multiple annotations, you can select the tab of each annotation by annotator and result ID. The annotation result ID is different from the task ID visible in the left menu. 

You can assign reviewers to tasks, or people with access can review tasks on an ad hoc basis. Anyone who is assigned to a task or who completes a review of a task appears in the Reviewers column on the Data Manager. You can assign reviewers to multiple tasks at once, but you cannot remove reviewers from multiple tasks at once. 


## Verify model and annotator performance 


### Review annotations against ground truth labels 
There isn't a way to set ground truth labels rn I don't think.

### Review annotator consensus 