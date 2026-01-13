This project involves developing an AI-powered conversational chatbot capable of understanding and responding to user queries in real time. The chatbot uses natural language processing (NLP) and pretrained transformer models (DialoGPT) to provide human-like responses, making it suitable for customer support, FAQs, and interactive web or mobile applications.

Key Features:
Conversational AI: Understands user inputs in natural language and responds appropriately.
Context Awareness: Maintains context over multiple turns in a conversation
Scalable: Can be integrated with websites, mobile apps, or messaging platforms.
Customizable Knowledge Base: Can be adapted to specific domains, like e-commerce, education, or healthcare.

Technical Details:
Language: Python
Libraries: transformers, torch
Model Used: microsoft/DialoGPT-medium
Input: User text queries (e.g., "What products do you offer?")
Output: AI-generated text responses (e.g., "We offer AI tools for education, healthcare, and business.")

Use Cases:
Customer support automation
FAQ bots for websites
Virtual assistants for small businesses

Example Interaction:
User: Hi, can you tell me about your products?
Chatbot: Sure! We offer AI tools for education, healthcare, and business.
User: What is the price range?
Chatbot: Our products range from free trials to premium enterprise solutions.


Impact:
This project demonstrates hands-on experience in NLP, transformer-based models, and AI-driven customer service automation, making it a valuable addition to a portfolio or resume.

code:
responses = {
    "hi": "Hello! How can I help you today?",
    "hello": "Hi there! How can I assist you?",
    "products": "We offer AI tools for education, healthcare, and business.",
    "price": "Our products range from free trials to premium solutions.",
    "bye": "Goodbye! Have a great day!",
    "hello": "How can i help you.",
    "thankyou": "Your Welcome.",
}

print("Chatbot: Hi! I'm your assistant. Type 'exit' to end the chat.")

while True:
    user_input = input("You: ").lower()  # take user input
    if user_input == "exit":             # exit condition
        print("Chatbot: Bye! Chat ended.")
        break

    # Check if any keyword in responses matches user input
    found = False
    for key in responses:
        if key in user_input:
            print("Chatbot:", responses[key])
            found = True
            break

    if not found:
        print("Chatbot: Sorry, I didn't understand that.")
