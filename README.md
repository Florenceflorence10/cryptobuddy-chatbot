# cryptobuddy-chatbot

class Cryptobuddy:
    def __init__(self):
        self.rules = {
            "hey": "Hey there! Let's find you a green working crypto.Type 'green'",
            "green": "So here are some of the working cryptos. Type 'three' to view them all.",
            "three": "They include Bitcoin, Ethereum and Cardano.",
            "tell me about each one of the cryptos": "Type 'Bitcoin', 'Ethereum' or 'Cardano'.",

            "bitcoin": "Type 'info' to acquire information about Bitcoin.",
            "info": "Bitcoin is the first digital money that you can send without needing a bank. It works on a blockchain, which is like a public digital record book. It is decentralized, meaning no one including the government can control it.it's price trend is stable,market cap is high,has medium energy use and it's sustainability score is 6/10    .",
           
            "ethereum": "Type 'details' to acquire clear details about Ethereum.",
            "details": "Ethereum is used to pay transactions, invest or run smart contracts.It has a stable price trend,high market cap,medium energy use and it's sustainability score is 6\10",
           
            "cardano": "Type 'more about' to acquire more information on Cardano.",
            "more about": "ADA is the digital coin used on the Cardano blockchain. It's named after Ada Lovelace, the first computer programmer.Has a rising price trend,medium market cap,low energy use and it's sustainability score is 8/10",

            "what is the most sustainable coin": "Cardano!",
            "which crypto is trending up?":"bitcoin and cardano",
            "which coin is profitable": "For profitability, consider Bitcoin.",
            "i highly appreciate": "Anytime dearest!",
            "help": "start by typing bitcoin"
            
        }

    def get_response(self, message):
        message = message.lower().strip()
        for pattern in self.rules:
            if pattern in message:
                return self.rules[pattern]
        return "Sorry, I don't understand that. Try saying 'help'."

# Interactive chatbot
if __name__ == "__main__":
    chatbot = Cryptobuddy()
    print(" Type hey  to start.\n")

    while True:
        user_input = input("You: ")
        if user_input.lower() in ["exit", "quit", "bye"]:
            print("Cryptobuddy: Goodbye!")
            break
        response = chatbot.get_response(user_input)
        print("Cryptobuddy:", response)
        
