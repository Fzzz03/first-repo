# What is AI?

Imagine you have a super-smart robot that learns like you do. You show it lots of cat pictures, and instead of explaining every detail, it figures out what makes a cat a cat by noticing patterns all by itself. That’s AI in a nutshell: teaching computers to learn from data so they can make decisions without step-by-step instructions.

In trading, AI acts like a tireless, lightning-fast assistant. It analyzes huge amounts of data, spots trends, and even predicts what might happen next—all by recognizing patterns in the numbers. It’s not magic; it’s simply very good at crunching data, which makes it a powerful tool in the fast-paced world of finance.

# AI, Machine Learning, and Deep Learning: How They Connect
You’ve probably heard terms like AI, machine learning, and deep learning. Here’s how they fit together:
You may have come across terms like AI, Machine Learning, Deep Learning, and Neural Networks. But how are they connected?

**AI (Artificial Intelligence):** The broad idea of making machines smart—helping them think, learn, and make decisions.  
**Machine Learning (ML):** A subset of AI where computers learn from past data without being explicitly programmed.  
**Deep Learning (DL):** A more advanced type of ML that uses artificial neural networks (inspired by the human brain) to make complex decisions.  
**Neural Networks:** The backbone of deep learning, helping computers recognize patterns in data, like images, text, or stock prices.

(Note: Include the diagram ![aimlbox](images/aimlbox.png) here to visualize this relationship!)

---

## B. Types of Machine Learning

There are three main types of machine learning—let’s break them down with examples and trading applications:

(Note: Include the diagram ![ML-Types](images/ML-Types.png) here for a visual overview!)

1. **Supervised Learning**  
   **Definition:** The model is trained on labeled data, meaning it learns from examples that already have correct answers.  
   **Example:** A spam filter that learns to identify spam emails by analyzing past emails labeled as spam or not spam.  
   **Trading Example:** A trading bot is trained on historical stock prices with labeled outcomes (whether the price went up or down). It learns patterns to predict future prices and make trades accordingly.

2. **Unsupervised Learning**  
   **Definition:** The model is given data without labels and must find patterns or relationships on its own.  
   **Example:** Customer segmentation, where an e-commerce website groups users based on their shopping behavior without knowing in advance what the groups should be.  
   **Trading Example:** A trading bot clusters stocks based on similarities in their price movements, helping traders identify groups of stocks that tend to move together.

3. **Reinforcement Learning**  
   **Definition:** The model learns by interacting with an environment and receiving rewards or penalties based on its actions.  
   **Example:** A self-driving car that learns to navigate by getting rewards for safe driving and penalties for mistakes like crossing lanes or stopping too late.  
   **Trading Example:** A trading bot learns by trial and error, testing different trading strategies and adjusting based on the profit or loss it makes.

**Challenge:** Can you think of another example for each type of machine learning?

---

## III. Deep Learning and Neural Networks

### A. What is Deep Learning?
Deep learning is a type of AI that uses something called neural networks (like a virtual brain) to learn from data. It’s great at finding complex patterns in large amounts of data, like stock prices, news, and trends.

### B. How Artificial Neurons Are Inspired by the Human Brain
Artificial neural networks (ANNs) are inspired by the structure and function of the human brain:

- **In the Brain:**  
  Neurons receive inputs through dendrites, process signals in the cell body, and pass the signal via the axon.  
  Synapses strengthen or weaken connections based on learning.

- **In an ANN:**  
  Artificial neurons receive numerical inputs, apply a function (like activation functions), and pass signals to the next layer.  
  Weights and biases adjust during training to "learn" patterns, similar to how synapses adjust in the brain.

(Note: Include the diagram ![Ann-inspired-human](images/Ann-inspired-human.png) here to show this comparison!)

### C. How ANNs Led to Deep Learning
ANNs started as simple models but evolved into deep learning as computational power increased. Early ANNs had a few layers, but deep learning introduced deep neural networks (DNNs) with many hidden layers, allowing models to learn much more complex patterns.

**What Deep Learning Adds Compared to Traditional Machine Learning:**

- **Feature Learning:** Instead of relying on manually crafted features, deep learning discovers the best features automatically.
- **Scalability:** Deep learning can process vast amounts of data, like financial transactions or stock market trends, without losing efficiency.
- **Hierarchical Representation:** Lower layers detect basic patterns (e.g., price fluctuations), while higher layers recognize complex patterns (e.g., market trends and sentiment).

### D. Deep Learning Workflow for Trading Bots
Here’s how a trading bot uses deep learning—step by step:

(Note: Include the diagram ![deepLearningFlow](images/deepLearningFlow3.png) here to illustrate this workflow!)

#### Define the Goal:
The bot’s job is to predict whether a stock will go up or down based on data like stock prices, news, and trends.

#### Collect Data:
Gather lots of information for the bot to learn from:
- **Stock Prices:** Historical data (e.g., Apple’s stock prices for the last 5 years).
- **News Articles:** Headlines like “Apple releases new iPhone” or “Tesla recalls cars.”
- **Social Media Trends:** What people are saying about companies on Twitter or Reddit.

#### Prepare the Data:
Clean and organize the data so the bot can understand it:
- Convert text (news, social media) into numbers (e.g., “good news” = 1, “bad news” = 0).
- Normalize stock prices so they’re on the same scale (e.g., between 0 and 1).

#### Build the Neural Network:
The bot uses a neural network (a virtual brain) to learn from the data.
- At first, the neural network is untrained—it knows nothing and makes random predictions.

#### Train the Neural Network:
Feed the data into the neural network and let it learn:
- **Example:** Show the bot Apple’s stock prices and news from the past.
- The bot tries to predict if the stock went up or down.
- If it’s wrong, it adjusts itself to get better next time (this is called learning).

#### Test the Bot:
After training, test the bot on new data it hasn’t seen before:
- **Example:** Give it recent stock prices and news.
- Check if its predictions (up or down) are correct.

#### Use the Bot:
Once the bot is trained and tested, it’s ready to make predictions:
- **Example:** The bot sees news like “Apple releases new iPhone” and predicts the stock will rise. It automatically buys Apple stock for you.
- If it predicts the stock will fall, it sells to avoid losses.


# Evolution of AI in Finance

AI in finance didn’t happen overnight. Here’s how it grew:


# Stage 1: Rule-Based Systems

Back in the day, computers used rule-based systems—simple “if this, then that” instructions.

**Example:** “If a stock hits its 50-day average, buy it.”  
**Limit:** No flexibility—markets change, but rules didn’t.

# Stage 2: Machine Learning

Then came machine learning, letting computers learn from data, not just follow orders.

**Example:** ML spots that a stock rises after big news and adapts to predict it.

# Stage 3: Deep Learning

Now, deep learning rules the roost, using neural networks to tackle huge datasets.

**Example:** DL scans social media and predicts stock swings from public mood.

---

**Big Win:** It’s fast, flexible, and insanely powerful.

