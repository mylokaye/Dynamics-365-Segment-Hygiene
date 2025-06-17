# Dynamics 365 Segment Hygiene (Filter out bad records)

A powerful and customizable query designed for Microsoft Dynamics 365 Customer Insights - Journeys (formerly Marketing), enabling marketers and CRM admins to create dynamic segments to filter ourt bad / poor quality records. 

This query filters contacts whose first names are either: empty, contains a period, or single character. making it ideal for filtering out bad contact records so that you can send personliased campaigns without worrying.

# 📂 **First Name Query Filter**

PROFILE(contact, contact_1)
    .FILTER(contact_1.firstname == 'A' || contact_1.firstname == 'B' || contact_1.firstname == 'C' || contact_1.firstname == 'D' || contact_1.firstname == 'E' || contact_1.firstname == 'G' || contact_1.firstname == 'H' || contact_1.firstname == 'I' || contact_1.firstname == 'J' || contact_1.firstname == 'L' || contact_1.firstname == 'M' || contact_1.firstname == 'N' || contact_1.firstname == 'P' || contact_1.firstname == 'R' || contact_1.firstname == 'S' || contact_1.firstname == 'X' || contact_1.firstname == 'd' || contact_1.firstname == 'x' || contact_1.firstname == '.' || contact_1.firstname == '-' || ISNULL(contact_1.firstname))

# 📂 **Email Query Filter**

FILTER(
  Contact.emailaddress1 MATCHES_REGEX "^[\\w\\.-]+@[\\w\\.-]+\\.\\w{2,}$"
)


# 🔍 **Features**

✅ Ready-to-use for Dynamics 365 Customer Insights - Journeys

🔠 Filters bad contat data by first name and email

🧼 First Name: Filters null, punctuation, lowercase edge cases

🧩 Email: One or more word characters, dots, or hyphens before the @, A domain name with similar characters, A top-level domain with at least two characters

📊 Ideal for excluding bad data for personalsied campaigns


# 🛠️ **How to Use**

1) Open Dynamics 365 Customer Insights - Journeys

2) Navigate to Segments

3) Choose New > Query (Designer)

4) Paste the query/s into the query editor

5) Save and go live to use in journeys or analytics



# 📌 Notes

This query uses the PROFILE entity and assumes contact_1 is the alias for the contact table.
You can modify the list of initials or add additional filters as needed.
I will add to this code over time to expand the filtering.


# 📢 **Contributing**

Feel free to fork this repo and submit a pull request if you have improvements or additional use cases! 💡
