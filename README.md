# Dynamics 365 Segment Hygiene (Filter out bad records)

📝 **Description**
A powerful and customizable query designed for Microsoft Dynamics 365 Customer Insights - Journeys (formerly Marketing), enabling marketers and CRM admins to create dynamic segments to filter ourt bad / poor quality records. 

This query filters contacts whose first names are either: empty, contains a period, or single character. making it ideal for filtering out bad contact records so that you can send personliased campaigns without worrying.

📂 **Query Overview**

PROFILE(contact, contact_1)
    .FILTER(contact_1.firstname == 'A' || contact_1.firstname == 'B' || contact_1.firstname == 'C' || contact_1.firstname == 'D' || contact_1.firstname == 'E' || contact_1.firstname == 'G' || contact_1.firstname == 'H' || contact_1.firstname == 'I' || contact_1.firstname == 'J' || contact_1.firstname == 'L' || contact_1.firstname == 'M' || contact_1.firstname == 'N' || contact_1.firstname == 'P' || contact_1.firstname == 'R' || contact_1.firstname == 'S' || contact_1.firstname == 'X' || contact_1.firstname == 'd' || contact_1.firstname == 'x' || contact_1.firstname == '.' || contact_1.firstname == '-' || ISNULL(contact_1.firstname))
    

🔍 **Features**

✅ Ready-to-use for Dynamics 365 Customer Insights - Journeys

🔠 Filters contacts by first name initials

🧼 Includes null, punctuation, and lowercase edge cases

🧩 Easily extendable for additional conditions

📊 Ideal for segmenting large contact datasets


🛠️ **How to Use**

Open Dynamics 365 Customer Insights - Journeys

Navigate to Segments

Choose New > Query (Designer)

Paste the query into the query editor

Save and go live to use in journeys or analytics



📌**** Notes****

This query uses the PROFILE entity and assumes contact_1 is the alias for the contact table.
You can modify the list of initials or add additional filters as needed.


📢 **Contributing**

Feel free to fork this repo and submit a pull request if you have improvements or additional use cases! 💡
