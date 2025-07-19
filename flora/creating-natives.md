---
layout: default
title: Creating Natives
parent: Flora
grand_parent: Home
nav_order: 1
---

# Creating Natives

Native records are fundamental to your flora management system. These records have no dependencies and should be created first.

{: .label .label-blue }
Foundation Model

## Prerequisites

- Management access or administration panel access
- No model dependencies (can be created first)

## Step-by-Step Guide

### Step 1: Navigate to Management Section

1. **Access the navbar** at the top of the website
2. **Click on "Management"** in the main navigation menu
3. **Scroll down to find "Flora"** in the management section
4. **Click on "Flora"** to expand the flora options

<img src="{{ '/assets/images/flora/flora_navbar.jpeg' | relative_url }}" 
     alt="Flora Navigation" 
     class="img-small">
<p><em>Figure 1: Navigating to Flora management section</em></p>

### Step 2: Access Natives

1. **Click on "Natives"** from the flora submenu
2. This will take you to the natives list view

### Step 3: Create New Native

1. **Click the "Create" button** (usually a green "+" icon or "Add" button)
2. This opens the native creation form

![Create Natives Button]({{ '/assets/images/flora/native_listview_create_button.jpeg' | relative_url }})
*Figure 2: Create button for natives*

### Step 4: Fill Out the Form

Complete all required fields in the native form:

![Natives Form]({{ '/assets/images/flora/native_create_form.jpeg' | relative_url }})
*Figure 3: Native creation form*

#### Required Fields

- **Scientific Name**: The botanical name (e.g., *Eucalyptus saligna*)
- **Common Name**: Local or common name (e.g., Blue gum, Sydney blue gum)

#### Optional Fields

- **Notes**: Additional information
- **Is Active:** Leave this checked (True)
   - *Purpose*: Controls record visibility without deletion
   - *Why?* Deleting records can break connections to other data
   - *Usage*: 
       - `True` = Record appears in lists and can be used
       - `False` = Record is hidden but data is preserved


### Step 5: Save the Record

1. **Review all entered information** for accuracy
2. **Click "Create"** to create the native record
3. **Verify creation** by checking the success message

## Data Entry Tips

{: .highlight }
**Best Practices**
- Use proper botanical naming conventions
- Include both scientific and common names

{: .warning }
**Validation Rules**
- Scientific names must be unique
- Required fields cannot be empty

## Related Models

Once weeds are created, they can be referenced by:

- **Site Reports** 

## Next Steps

After creating native plants, you can proceed to:

1. [Creating Weed Species](creating-weeds)
2. [Creating Tool Types](../tools-equipment/creating-tool-types)
3. [Creating Work Types](../work-categories/creating-work-types)

---

{: .fs-2 }
[Back to Flora Index](index){: .btn .btn-outline }
[Foundation Models](../index){: .btn .btn-outline }