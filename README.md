# Chatbot-using-Amazon-Lex-Hotel-Booking

This project implements a chatbot Book-H is designed to facilitate hotel reservations through natural language interactions, to automate the hotel room booking process. The chatbot assists users in selecting room types, providing pricing information, and managing booking confirmations. By automating these tasks, the system enhances the user experience, making hotel room booking seamless and efficient.

**Features**
Room Type Selection: Users can inquire about different room types such as Classic, Deluxe, Suite, and Duplex.
Pricing Information: The bot provides pricing details for each room category.
Step-by-step Booking: Users are guided through the booking process, including room type selection, check-in date, and duration of stay.
Confirmation: The bot confirms booking details (e.g., room type, check-in date, and stay duration) and provides a final confirmation message.

**Tools and Technologies**
Amazon Lex: Manages user interactions and handles natural language understanding for booking requests.
AWS Lambda: Used to execute the fulfillment logic and process user inputs.
Amazon DynamoDB (Optional): Can be integrated for storing and retrieving booking details.
AWS CloudWatch: Used for monitoring and logging the system.
AWS IAM: Ensures secure access control for Lex and Lambda resources.

**Project Breakdown**
1. Amazon Lex Setup
The chatbot was configured in Amazon Lex, leveraging the BookHotelRoom intent, which gathers information such as room type, check-in date, and duration of stay. The bot handles several sample utterances, including:

"Are any rooms available?"
"Need to book rooms."
"Need rooms."

2. Slot Types
The chatbot uses custom and predefined slot types to collect necessary information:

RoomType: Custom slot for room categories (Classic, Duplex, Suite).
CheckInDate: Captures the user’s check-in date.
DurationOfStay: Collects the number of days for the stay.
Confirmation: Yes/No slot type to confirm the booking.

3. Fulfillment Logic
Once the user provides all necessary information, the fulfillment logic confirms the booking with a response like:

Your Booking Confirmed. You have selected a {RoomType} room for {DurationOfStay} days. You will check in on {CheckInDate}. Thank you for choosing our hotel.
Fallback logic is implemented to handle invalid inputs.

**Testing and Results**
Extensive testing was carried out to ensure the chatbot's accuracy and reliability. The system was tested across various scenarios:

Booking different room types.
Verifying the flow for different durations of stay.
Ensuring that pricing and booking confirmation are consistent.
Future Improvements
Dynamic room types and seasonal pricing.
Integration with external hotel booking APIs to retrieve real-time availability.
Expanded language support and enhanced features like booking modifications and cancellations.

**Conclusion**
The Hotel Booking Chatbot using Amazon Lex successfully automates the hotel room booking process, providing users with a streamlined and intuitive experience. The system demonstrates the potential for leveraging cloud-based chatbot technology in the hospitality industry to enhance user engagement and efficiency.
