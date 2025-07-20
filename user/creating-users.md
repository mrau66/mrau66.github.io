---
layout: default
title: Creating Users
parent: Users
grand_parent: Home
nav_order: 1
---

# Creating Users

User records are fundamental to our system, serving as the foundation for access control, permissions, and tracking user activities throughout the application. Each user record contains personal information, account credentials, address details, default pay scale and work experience data.

{: .label .label-blue }
Foundation Model

## Prerequisites

- Management access or administration panel access
- Active pay scales must exist before creating users
- Understanding of user roles and permissions (roles should be already been prepopulated by system.)

## Step-by-Step Guide

### Step 1: Navigate to Management Section

1. **Access the navbar** at the top of the website
2. **Click on "Management"** in the main navigation menu
3. **Scroll down to find "Users"** in the management section
4. **Click on "Users"** to expand the user management options

<img src="{{ 'assets/images/users/user_staff_navbar.jpeg' | relative_url }}" 
     alt="Users Navigation" 
     class="img-small">
<p><em>Figure 1: Navigating to Users management section</em></p>

### Step 2: Access User Creation

1. **Click on "Staff"** from the user management submenu
2. This will take you to the staff list view

### Step 3: Create New User

1. **Click the "Create" button** (usually a green "+" icon or "Add" button)
2. This opens the user creation form with broadly five sections

![Create User Button]({{ 'assets/images/users/user_listview_create_button.jpeg' | relative_url }})
*Figure 2: Create button for users*

### Step 4: Fill Out the User Creation Form

The user creation process involves five forms:

![User Creation Forms 1 & 2]({{ 'assets/images/users/create_user_form_1.jpeg' | relative_url }})
![User Creation Forms 3, 4 & 5]({{ 'assets/images/users/create_user_form_2.jpeg' | relative_url }})

*Figure 3: User creation form with five sections*

#### Section 1: User Information (Required)

**Personal Details:**
- **First Name**: User's first name (required)
- **Last Name**: User's last name (required)
- **Email**: Unique email address (required)
- **Phone**: Contact phone number (optional)
- **Password**: Strong password following security requirements
- **Confirm Password**: Re-enter password for verification

#### Password Requirements

{: .highlight }
**Password must meet these criteria:**
- At least 8 characters long
- Cannot be too similar to personal information
- Cannot be a commonly used password
- Cannot be entirely numeric

#### Section 2: 
**Email Verification Settings**
- Process to verify e-mail by sending system e-mail, containing a link, to the new user's e-mail.
- **Mark email as verified**(required): Skip email verification process.  We know user's e-mail exists and has been manually verified.
- **Set as primary email**(required) Make sure it is checked true.

#### Section 3: 
**AssignRole:**
- **Primary Role**: Choose user role (required)
  - Manager: Full system access
  - Supervisor: Almost full system access - no access to financial data 
  - Field Staff: Limited operational access - Generally, cannot edit, delete or create records. Does not have access to management. Can view reports and roster. Can edit their own details.

#### Section 4: 
**Pay Scale:**
- **Default Pay Scale**(required): Select from available pay scales (required)

#### Section 5: 
**Address:**
Complete address fields as needed:
- **Unit Number**: Apartment/unit number (numeric only)
- **Street Number**: House/building number (numeric only)
- **Street Name**: Street name
- **Street Type**: Avenue, Street, Road, etc.
- **Suburb**: Suburb or locality
- **State**: Select from dropdown
- **Postcode**: 4-digit postal code (numeric only)

{: .note }
**Address Validation**
- Unit number, street number, and postcode must contain only numeric characters
- Address information is optional but recommended for complete user profiles

**Prior Hours Worked**: Total work experience hours before joining (required)
  - Enter 0 if no prior experience
  - Must be a positive number or zero
  - This tracks relevant experience brought from previous employment

### Step 5: Save the User Record

1. **Review all entered information** across all three forms for accuracy
2. **Ensure required fields are completed**:
   - User Information: First name, last name, email, passwords, pay scale, role
   - Work Experience: Prior hours worked
3. **Click "Submit"** to create the user record
4. **Verify creation** by checking the success message

## Data Entry Tips

{: .highlight }
**Best Practices**
- Use proper email formatting
- Choose appropriate user roles based on job responsibilities
- Set realistic prior work hours
- Consider email verification settings based on security requirements

{: .warning }
**Validation Rules**
- Email addresses must be unique across all users
- All password requirements must be met
- Numeric fields (unit number, street number, postcode) accept only numbers
- Prior hours cannot be negative

## User Roles and Permissions

### Manager
- Full system access and administration
- Can manage all users, sites, financial data, and management tasks
- Financial and reporting access

### Supervisor
- Cannot edit, delete, view or create financial tasks i.e. purchase orders
- Can edit, delete, view or create reports,rosters and management tasks
- Can manage assigned teams and sites

### Field Staff
- Cannot edit, delete, view or create management tasks
- Can view reports and rosters
- Limited to own data and assigned tasks

## Email Verification

### Verified Email
- **Checked**: User can immediately access the system
- **Unchecked**: User must verify email before full access

### Primary Email
- **Checked**: This becomes the user's main communication email
- **Unchecked**: Email is added but not set as primary

## Related Models

Once users are created, they can be associated with:

- **Rosters and Roster Items**
- **Site Reports and Work Entries**
- **Incident Reports**
- **Hours Worked Records**
- **Training and Induction Records**

## System Integration

User creation automatically:

1. **Assigns group permissions** based on selected role
2. **Creates email address record** with verification status
3. **Sets up work experience tracking** with prior hours
4. **Establishes address record** if provided
5. **Generates user profile** for system access

## Troubleshooting

### Common Issues

**Email Already Exists**
- Error indicates another user has this email
- Check existing users or use different email address

**Form Validation Errors**
- Review all three sections for missing required fields
- Check numeric field formatting
- Verify password meets all requirements

**Role Assignment Issues**
- Ensure selected role exists in system
- Contact administrator if role options are missing

## Next Steps

After creating users, you can proceed to:

1. [Creating Rosters](../rosters/creating-rosters)
2. [Setting Up Training Records](../training/managing-training)
3. [Configuring Pay Scales](../payroll/managing-payscales)

---

{: .fs-2 }
[Back to Users Index](index){: .btn .btn-outline }
[Foundation Models](../index){: .btn .btn-outline }