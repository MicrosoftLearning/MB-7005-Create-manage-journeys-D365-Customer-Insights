---
lab:
    title: 'Lab 2: Create segments'
---

## Lab 2: Create segments 

In this lab, you will learn how to:
- Update information on customer records
- Create a segment 

### Task 1: Update the City for different customers

One of the journeys will target customers who live in a specific city. To ensure that you will have members in this segment, we need to add a city to each of the contacts that currently exist.

1. Log into **Dynamics 365 Customer Insights - Journeys**. Ensure you are in the **Real-time journeys** area.

1. Under Audience, select **Contacts.**

1. Select the first 10 contacts in the list. (Hint: holding the shift button while selecting a contact allows you to select multiple at once.)

1. On the command bar, select **Edit.**

1. In the Address 1: City field, enter **Seattle.**

1. Select the **Save** button.

1. Select the next 50 contacts in the list.

1. On the command bar, select **Edit.**

1. In the Address 1: City field, enter **Portland.**

1. Select the **Save** button.

1. Select the next 10 contacts in the list.

1. On the command bar, select **Edit.**

1. In the Address 1: City field, enter **Boise.**

1. Select the **Save** button.

1. Select the next 10 contacts in the list.

1. On the command bar, select **Edit.**

1. In the Address 1: City field, enter **Seattle.**

1. Switch to the **Details** tab. In the text box under **Personal notes**, enter **Business.**

1. Select the **Save** button.

### Task 2: Create a segment for Humongous Insurance customers

1. Navigate to **Segments**, under the Audience group.

1. Select **+New Segment.**

1. In the **Name the segment** box, enter **Humongous Insurance**. Select **Contact** as the target audience. Select **Create.**

1. Select **Add a new group** in the segment designer. First, we will choose an **Attribute group.**

1. From the Attributes pane, we will add the related table **Account.**
    - Select **+Add table** from the Related tables area.
    - Select **Account.**
    - Select **Next.**
    - Select **Add (1).**
    - The **Account** table will now appear under Related tables in the Attributes pane.

1. Expand **Account.**
    - Select the **Account** lookup.
    - Add item to **Existing group.**
    - Select **Group 1.**
    - Select the **Account > Contact** relationship and select **Next.**
    - Select **Company Name (Account)**.
    - Select **Set path.**

1. In the lookup in Group 1, select **Humongous Insurance.** The Group 1 condition will read "Account (Account) Is Humongous Insurance".

1. We want to add another condition to the segment. Select **+Add new** to add a new group and select **Attribute group.**

1. Change the operator to **or.**
    - In the Attribute pane, start typing **Email.** Expand **Contact.** Select the **plus** button next to the email field and add it to Group 2.
    - Create the following condition: **Email contains humongousinsurance**

1. Select **Save.**

1. Select **Ready to use** in the toolbar.

### Task 3: Create a business user segment

1. Navigate to **Segments** under the Audience group.

1. Select **+New Segment.**

1. Name the segment **Business Customers**. Keep **Contact** selected as target audience. Select **Create.**

1. Next, we will add **Account** as a related table for this segment.
    - Select **+Add table** from the Related tables area.
    - Select **Account.**
    - Select **Next.**
    - Select **Add (1).**
    - The **Account** table will now appear under Related tables in the Attributes pane.

1. Expand **Account.**
    - Select the **Account** lookup.
    - Add item to **Existing group.**
    - Select **Group 1.**
    - Select the **Account > Contact** relationship and select **Next.**
    - Select **Company Name (Account)**.
    - Select **Set path.**

1. In the lookup in Group 1, select **Contoso, Ltd.**

1. Select **Save** and then select **Ready to use.**

1. Wait for your segment to build.

### Task 4: Create a Contoso segment  
2.	Navigate to **Segments** under the Audience group. 

3.	Select **+New Segment. **

4.	Name the segment **Contoso Customers**. Keep **Contact** selected as target audience. Select **Create.**

5.	Add a new group and select **Create attribute group**. In the **Attributes** pane, expand **Contact** and add **Description** to Group 1. 

6.	In the segment designer, change the qualifier to **Contains**. For the value, enter **Business.**

7.	Select **Save** and then select **Ready for use.** 

8.	Wait for your segment to build. 

### Task 5: Create a Seattle customers segment
1. Navigate to Segments under the Audience group.

1. Select **+New Segment.**

1. Name the segment **Seattle Customers**. Keep **Contact** selected as target audience.

1. Select the **Create** button.

1. Add a new group and select **Create attribute group**. In the Attributes pane, expand **Contact > Address 1**, and add **Address 1: City** to Group 1.

1. In the segment designer, leave the qualifier as is. For the value, enter **Seattle.**

1. Select **Save** and then select **Ready to use.**

1. Wait for your segment to build.

### Task 6: Check your segment members 
It may take a few minutes or up to an hour for your segments to build. In the meantime, you can use them in a journey, but you won't be able to view your segment members until the segment is built. You can check the status of your segment in the **All segments** view and looking at the **Status reason** column. 

1. When your segment status reason is **Ready to use,** select the segment.
1. Navigate to the **Members and insights** tab.
1. View segment size and segment members. 
