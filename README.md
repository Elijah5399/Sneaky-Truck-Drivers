# NinjaSlot
![Screenshot 2023-02-26 at 3 48 49 PM](https://user-images.githubusercontent.com/22656175/221398673-9502cfa0-efb2-48b7-883a-db72c0d864bc.png)
### Our idea
To implement a scheduling functionality into NinjaChat on Telegram. What is the benefit of this, you may ask?

 Driver | Consignee | NinjaVan 
---|---|---
They get commission from completing these priority deliveries | They know with more certainty when their parcels will be delivered | Getting a cut from the service means a richer ninja!

### Features
- Sends a message to the consignees to inform them of the option to select time slots

    >In addition to the current message to allow consignees to add instructions for drop-off, they will now receive a message informing them of the option the select a time slot for the parcel to be delivered. This message will be sent once the parcel has been scanned and inbounded.
    >They will also be informed of the cutoff time of 0830, after which they will no longer be able to select any time slot.

- Option for consignee to select time slots

    > 4 time slots will be available:
    0900-1200, 1200-1500, 1500-1800, 1800-2000

    >Dynamic Pricing based on demand and supply factors, subject to a floor price.

    >A time slot option will no longer be available once the capacity has been reached (e.g. 1200-1500 option will no longer show on telegram once capacity has been reached).

- Option to cancel **before** cutoff time

    >Consignees would be able to cancel their selection of any time slot before the cutoff time.

- Payments

    >After the desired time slot has been selected, the bot will generate a link to an external site for payments (using Stripe in our implementation), but for actual implementation perhaps Ninja Finance can be adjusted to support this functionality.

### Technologies Used
- Java, Telegram Bot API, Huawei Cloud, Stripe API

### Java

- Key features of Java

 >We utilised Object-Oriented Programming (OOP) and followed OOP principles where possible. For instance, class fields are kept private to maintain an abstraction barrier, with public methods to modify and obtain data. (This is evident in the Day.java and Timeslot.java files)
    
 >We utilised Java's inbuilt interfaces and classes to our advantage, for instance in the use of Lists and ArrayLists in Bot.java.
    
### Telegram Bot API

 >We heavily utilised the Telegram Bot API, and heavily relied on its methods to retrieve data on messages/commands which the bot receives.
    
 >Some examples include the .getMessage and .getChatId methods.
    
### Huawei Cloud

 >We were able to set up an Elastic Cloud Server on Huawei Cloud, and upload files into it. 
    
### Stripe API

 >We used the Stripe API to make it possible for the user to submit a payment.
    
Note: To duplicate the bot, create a new bot using botFather and obtain the bot key. Also create an account and set up a payment link on stripe. Substitute the fields in the files with these. These files can be substituted in when a new project has been created on Intellij IDEA using Maven as a dependency manager. Add relevant modules and libraries in the project structure.

