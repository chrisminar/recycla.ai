---
layout: page_w_header
title: "Errors"
permalink: /errors
links:
  - text: "App setup"
    href: "app_setup"
  - text: "Device setup"
    href: "device_setup"
  - text: "Recycling"
    href: "recycling"
  - text: "Errors"
    href: "errors"
  - text: "Tips"
    href: "tips"
---

# Labeling
One of the most helpful things you can do as a tester is correct the Recycla when it labels incorrectly. Heres how

1. Tap the thumbnail tab

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label1.png' | relative_url }}" alt="label">
    </div>

2. Tap the image you want to correct

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label2.png' | relative_url }}" alt="label">
    </div>

3. Tap material

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label3.png' | relative_url }}" alt="label">
    </div>

4. Choose material type

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label4.png' | relative_url }}" alt="label">
    </div>

5. Choose submaterial.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label5.png' | relative_url }}" alt="label">
    </div>

    1. More information on material and sub material [here](recycling#taxonomy).
    2. The ground truth doesn't update in the cloud until you select a submaterial so don't select just a material.
    3. If you don't know what submaterial it should be you can choose the generic option.
    4. If you don't think your item has an appropriate representation in the taxonomy structure, follow the instructions [here](#reporting-common-errors) to report it.

6. Tap Category

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label6.png' | relative_url }}" alt="label">
    </div>

7. Choose an existing category or make a new one. The goal of this label is to understand what this item is, i.e. a Coke zero.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label7.png' | relative_url }}" alt="label">
    </div>

8. Tap and add a brand. The goal of this label is to understand who makes this item. i.e. Coca-Cola.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/labeling/label8.png' | relative_url }}" alt="label">
    </div>

9. Ignore Product, that is going away soon.

# Reporting Common Errors {#reporting-common-errors}

There are several common errors that you will likely encounter at some point that can be reported directly through the app. Recycla records a short video clip of motion, filters out uninteresting clips, then chooses the 'best' image from it to display to you and run the classification on. All of these steps can go wrong. The common errors are the first two steps going wrong. The classification going wrong is very common and you can help that with labeling (see above).

1. Bad preview image (off center). You have this problem if the the recycling item is not in the center of the image. 
    1. If this is happening frequently it could be a user issue. Try adjusting where you hold the item you are recycling and make sure you hold it there for a 1-2 seconds before dropping.
    2. It can also happen because Recycla choose the wrong image to display.
2. Bad preview image (blurry / item moving). You have this problem if the item in the image appers blurry.
    1. If this is happening frequently it could be a user issue. Make sure you hold the item steady for 1-2 seconds before dropping.
3. False positive. You have this problem if there is nothing in the preview window, or if the preview window is all black.
4. Something else. If you think something else went wrong with this process you can report it here.

### How to report common errors.  

1. Navigate to thumbnail tab. 

    <div style="text-align: center;">
      <img src="{{ '/images/errors/report/report1.png' | relative_url }}" alt="report">
    </div>

2. Tap the offending item in the thumbnail tab then tap report.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/report/report2.png' | relative_url }}" alt="report">
    </div>

3. Pick the appropriate error. There is also an option to report a custom error if needed.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/report/report3.png' | relative_url }}" alt="report">
    </div>

# Reporting other problems and feedback.
If you have suggestions, find a bug, or think something broke in the app this is how you can report that feedback.

1. In TestFlight tap on Recycla. Do no click open, that will open Recycla.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/report/feedback1.png' | relative_url }}" alt="Feedback">
    </div>

2. Tap send feedback. Include a screenshot if possible.

    <div style="text-align: center;">
      <img src="{{ '/images/errors/report/feedback2.png' | relative_url }}" alt="Feedback">
    </div>