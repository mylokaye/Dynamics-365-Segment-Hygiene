# Dynamics 365 Segment Hygiene (Exclude poor quality records)

A powerful and customizable set of queries designed for Microsoft Dynamics 365 Customer Insights - Journeys (formerly Marketing), enabling marketers and CRM admins to create dynamic segments to filter out poor quality records so you can send personliased campaigns with confidence.

The purpose of these queries is so that you can create a seperate segment of all contact records with bad data, which you can either exclude or send a non-personalised email. 

# 📂 **First Name Query Filter (Personalisation)**

🔠 Filters poor quality first name data, such as an empty field, period, or single characters.

```
PROFILE(contact, contact_1)
    .FILTER(contact_1.firstname == 'A' || contact_1.firstname == 'B' || contact_1.firstname == 'C' || contact_1.firstname == 'D' || contact_1.firstname == 'E' || contact_1.firstname == 'G' || contact_1.firstname == 'H' || contact_1.firstname == 'I' || contact_1.firstname == 'J' || contact_1.firstname == 'L' || contact_1.firstname == 'M' || contact_1.firstname == 'N' || contact_1.firstname == 'P' || contact_1.firstname == 'R' || contact_1.firstname == 'S' || contact_1.firstname == 'X' || contact_1.firstname == 'd' || contact_1.firstname == 'x' || contact_1.firstname == '.' || contact_1.firstname == '-' || ISNULL(contact_1.firstname))
```

# 🔍 **Query to Detect All-Caps First Names (Personalisation)**

```
FILTER(
  Contact.firstname MATCHES_REGEX "^[A-Z]+$"
)
```

# 📂 **Email Query Filter (Hygeine)**

🔠 Filters one or more word characters, dots, or hyphens before the @, A domain name with similar characters, A top-level domain with at least two characters.

```
PROFILE(contact, contact_1)
  .FILTER(
    contact_1.emailaddress1 CONTAINS '@' &&
    contact_1.emailaddress1 ENDSWITH '.com' &&
    contact_1.emailaddress1 != 'a@b.com'
  )
```

# 🔍 **Features**

✅ Ready-to-use for Dynamics 365 Customer Insights - Journeys

📊 Ideal for excluding bad data for personalsied campaigns, improving deliverability and hygiene.


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
