---
layout: page_w_header
title: "Recycle"
permalink: /recycling
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

# Recycling with Recycla

1. Make sure Recycla is on. It takes about 2 minutes to boot after powering on.

2. Open the recycla app

    <div style="text-align: center;">
      <img src="{{ '/images/recycle/recycle1.png' | relative_url }}" alt="Recycle">
    </div>

3. Ensure the recycla app reports ready status. There are two ways to do this.
    1. If you launch the app pop up will appear at the top indicating if it is ready. This will only happen if the app is being launched, not if the app is already open and you switch to it.  

        <div style="text-align: center;">
           <img src="{{ '/images/recycle/recycle2.png' | relative_url }}" alt="Recycle">
        </div>

    2. Navigate to the settings page. Look for the colored dot next to your pi identifier. Green indicates it's ready. You can tap and hold the dot to make it display more information about the status.

        <div style="text-align: center;">
           <img src="{{ '/images/settigns_page.PNG' | relative_url }}" alt="Recycle" width="300">
        </div>

    3. If you are not getting a ready status your best bet is to restart the Reyclca device. Then complain to Chris.

4. Time to recycle! Hold the item the full bin width away and in the center of the field of view.

    <div style="text-align: center;">
      <img src="{{ '/images/recycle/recycle3.png' | relative_url }}" alt="Recycle">
    </div>

5. Hold for 1-2 seconds, then drop.

    <div style="text-align: center;">
      <img src="{{ '/images/recycle/recycle4.png' | relative_url }}" alt="Recycle">
    </div>

6. The app will show the Recycla is processing. Wait until it displays ready status before recycling again.

    <div style="text-align: center;">
      <img src="{{ '/images/recycle/recycle5.png' | relative_url }}" alt="Recycle">
    </div>

# Understanding Recycling Taxonomy (Material & SubMaterial) {#taxonomy}

Recycla uses a hierarchical taxonmy to catagorize and understand recycling. It has two levels. Materials and Sub Materials. The Material is what the object is made out of. Sub material is a bit more specific. Some of the Materials have a "Generic" sub material. This is a catch all for items of that material that don't have a more specific classification.

<div style="text-align: center;">
  <img src="{{ '/images/recycle/Taxonomy.png' | relative_url }}" alt="Taxonomy">
</div>

Here are some examples of the more confusing items in the taxonomy.

- Glass container: Glass items that look like mason jars
- Aluminum/Steel Aerosol
  - Steel cans are heavier than aluminum.
  - Steel cans often have a seam running along the side and the bottom is typically flat.
  - Aluminum cans usualy have a curved bottom that angles inwards.
- Plastic Tub: E.x. Yogurt or cream cheese container.
- Tetra Pak: These are containers used to store fluids. E.x. Orange juice carton. 
- Sprial Wound Cannister: E.x. Pringles container
- Compost: Non recyclable waste that is compostable.
- Waste: All things that are not recycle, wouldn't commonly be mistaken for recycle, and are not compostable.
- Miscellaneous: A few categories for things that are not disposeable.