## Notes
# Statistical Games: A Playful Approach to Understanding Statistics and Decision-Making
# URL 
https://arxiv.org/pdf/2402.15892.pdf
### Audio Version
- You can listen to the audio version [here](https://github.com/bhaskatripathi/MyPhDBookshelf/raw/main/audio/Statistical_Games.mp3).

Recently, I came across this very interesting paper that presents a new kind of mathematical philosophy. This is one of the longest papers that I have ever read and seems to be more like a text book with complex mathematical formulations but I have tried to simplify to the best of my understanding and distill the key ideas in simpler terms for layman audience. While the paper is dense in parts, it puts forth a creative gaming paradigm for reimagining statistics on more philosophical and practical foundations. Personally, as an avid reader of mathematical perspectives, I found the concepts quite fascinating despite needing to digest significant mathematical intricacies. It appears to be an ambitious step toward formalizing statistical uncertainty in a fresh yet coherent way.

It explores how we can use games to better understand statistics and decision-making, making complex ideas simpler and more connected. The paper introduces "statistical games" to unify two major statistical approaches, showing how decisions in uncertain situations can be thought of as part of a game. This innovative angle promises to change the way we approach problems in statistics, economics, and beyond.

## Summary

1. The paper suggests a novel and thought-provoking idea: using statistical games as a foundation for understanding statistical inference, which is the process of drawing conclusions from data. This approach is quite different from traditional views, which typically base statistical concepts on personal belief or the notion of randomness.
1. For example, consider a game where you're trying to guess the number of marbles in a jar based on a few samples you can see. Traditionally, you might guess based on your gut feeling (subjective belief) or by calculating probabilities based on the sample (chance). The paper suggests framing this as a game where your strategy for guessing is informed by statistical principles. The better your strategy, the more accurately you can infer the total number of marbles. This approach grounds statistical thinking in the concrete steps and decisions of game play, rather than abstract concepts of belief or randomness.
1. The paper introduces an innovative concept called "statistical games," which are designed to offer a new perspective on understanding statistical inference and probability through the lens of game theory. These games aim to bridge the gap between two major statistical approaches: Bayesian and Frequentist methodologies, by suggesting that the differences between these approaches can be seen as variations in risk aversion within the game's context. A generalized betting game called a "**Statistical game**" is introduced, which can **unify Bayesian** and **Frequentist games** by interpreting them as Statistical games differing only in risk aversion.

## Main Motivations

Statistics and probability theory are very successful in providing useful tools for research and real-world problems. However, there is still debate around interpreting concepts like probability.  The paper argues that while current techniques work well, the field lacks a unified structure and philosophy to tie everything together. This can cause unease for students learning statistics or professionals applying techniques if they don't fully understand how it connects to a bigger picture.

`    `The goal is to take a step back and look at statistics from a fresh perspective, trying to understand the core tasks where statistical ideas arise. The hope is this broader scope can then lead to a simpler, more coherent framework for statistics. The proposed approach is to view statistics through the lens of game theory - formulating decision problems with uncertainty as games between players. Things like making inferences from data can be cast into a game. Ideally this unified perspective can empower those who care about handling uncertainty, by equipping them with formulas, algorithms, and code rooted in a philosophically sound framework.

**Notes:**
## Bayesian vs. Frequentist Approaches
Bayesian and Frequentist refer to two different approaches in statistics:

**Frequentist Approach:**
- Relies only on frequency/proportion of outcomes in repeats of an experiment
- Does not incorporate a prior probability, only observes data
- Examples: sampling distribution, p-values

**Bayesian Approach**:
- Specifies a prior probability for possible outcomes/hypotheses
- Updates probabilities based on observed data to get a posterior distribution. New believes are formed on basis of updating past believes as more and new observations are obtained.
- Incorporates both prior belief and data

**Frequentist Game**: Likely a game scenario where one player provides/selects data samples, while the other player makes inferences solely based on frequencies of outcomes, ignoring priors.

**Bayesian Game**: A scenario where there is an initial probability distribution, which gets updated sequentially based on data samples from an adversarial player.

The key innovation of the paper is to unify these two types of games under one "**Statistical Game**" framework that can represent both **Bayesian** and **Frequentist** game dynamics through adjusting parameters like the agent's risk aversion.

**Prior and Posterior Probabilities:**

Prior probability refers to a probability that is assigned before observing any data or evidence. Some key points:

- It encodes an initial degree of belief about something being true before evidence is considered
- This could be based on logical deduction, previous information, subjective judgment, assumptions etc.
- Using Bayes' theorem, the prior probability gets updated based on new evidence to give a posterior probability.

A simple example is flipping a coin. We could assign:

- Prior probability of heads = 0.5

Meaning we start with an assumption of the coin being fair and heads/tails equally likely. We then flip the coin 10 times and get 6 heads and 4 tails. This is the "evidence" or data. 

The prior would then get updated to the posterior probability: P(heads | 6 out 10 flips were heads) = 0.6

So, the prior probability (0.5) gets shifted based on the evidence to determine a posterior (0.6).

**Binary Decision in Statistical Games:**

In these games, two players are involved, where one player (Player 2) chooses between two scenarios and creates a binary sequence. The other player (Player 1) then samples bits from this sequence to guess the chosen scenario. The section delves into trivial cases like blind guessing and sure winning, as well as the smallest nontrivial case, where it's feasible to enumerate all possible actions and outcomes to find equilibrium strategies. The main intuition is to explore how players' strategies in guessing and choosing scenarios can model binary decision-making processes, with implications for understanding statistical inference through game theory.

**Bayesian Betting:**

Bayesian betting refers to a betting or wagering scenario where Bayesian probability and inference is used to make decisions. The key elements of Bayesian betting are:

1. Prior Probabilities: At the outset, prior probabilities are assigned to each potential outcome that can be bet on. This encodes the initial belief about how likely each outcome is before seeing any evidence.
1. Updating Based on Evidence: As relevant evidence comes in, for example new data about a sports team's record, the probabilities get updated using Bayes' theorem. This results in posterior probabilities.
1. Betting Based on Posterior Probability: One would then place bets based on the posterior probabilities, which now reflect both prior belief and evidence. You would risk more money on outcomes that have higher probability as per the posterior distribution.

For example, there could be a 40% prior chance Team A wins their next game based on historical stats. After seeing new injury information, this could get updated to a 25% posterior probability of winning. A Bayesian bettor would then bet less money on Team A based on the revised lower probability.

In this way, the bets always reflect current probability estimates rather than relying on gut feelings. As new evidence comes in, the probabilities update in a rigorous mathematical Bayesian fashion.

`    `It involves games model situations where players bet based on prior beliefs about different scenarios, adjusting these beliefs as new evidence or data is collected. The core intuition behind Bayesian betting is that it simulates the process of making decisions with incomplete information, using Bayesian updating to adjust probabilities. Players start with initial beliefs (priors) about the likelihood of various outcomes and then refine these beliefs (posterior probabilities) as they gain more information. This dynamic reflects real-world decision-making processes, where choices are often made under uncertainty, and information is gradually revealed over time.

`    `In a typical Bayesian game, there are two players: one who chooses a scenario from a set of possibilities, and another who makes bets based on the observed outcomes of these scenarios. The game explores how the betting player uses Bayesian updating to improve their strategy, aiming to maximize their utility or payoff. This involves calculating the expected utility of different actions based on the updated probabilities and choosing the action that offers the highest expected utility.

**Example:**

**Statistically Trivial Case**: Imagine a game where a player has to guess whether a coin flip will result in heads or tails, knowing the coin is biased to land heads 75% of the time. In this scenario, the Bayesian approach would suggest betting on heads every time, as it's the outcome with the higher prior probability. This illustrates how Bayesian betting starts with an initial belief (the bias) and uses it to make decisions.

**Adopting a Utility Function**: Consider a scenario where a player must decide whether to bet on a single roll of a biased die, with the outcome significantly impacting their overall wealth. By adopting a utility function that weighs outcomes based on their risk preference (e.g., risk-averse, risk-neutral, risk-seeking), the player uses Bayesian updating to decide not just on the most likely outcome, but on the outcome that optimizes their expected utility, taking into account both probability and the utility of potential gains or losses.

**General Bayesian Game Description**: In a more complex game, two players are involved in predicting the outcome of a series of events, with one player trying to mask the true pattern of events while the other uses Bayesian updating to infer and bet on that pattern. For example, if player A chooses a sequence of biased coin flips (heads or tails) and player B has to bet on each outcome after observing a few flips, player B uses the observed outcomes to update their beliefs about player A's strategy and make informed bets. This scenario demonstrates how Bayesian updating facilitates strategic thinking in games by incorporating both prior beliefs and new information to refine decision-making strategies.

**Binomial and Fisher Games and Limiting policies**

When the number of trials or observations (N) becomes very large, approaching infinity. Below, I am trying to explain how these statistical games evolves and what kind of patterns or equilibria would emerge under these limiting conditions:

- **Binomial Games:** These are statistical games involving a series of trials with two possible outcomes. The section probably details how these games are structured and played, differentiating between the Fisher and Bayesian approaches.
  - **Binomial Fisher Games:** These games might focus on the Frequentist approach, where decisions are made based on the proportion of outcomes observed in repeated trials. The goal is to understand how the game's dynamics change as the number of trials increases indefinitely.
  - **Binomial Bayesian Games:** Here, the emphasis would be on incorporating prior beliefs into decision-making and updating these beliefs as more data (outcomes of trials) become available. The section likely examines how Bayesian updating impacts the strategies and outcomes of the game in the limit of many trials.
- **Limiting Policies for N → ∞:** This subsection probably discusses the theoretical implications of increasing the number of trials to infinity. It might explore questions like how the strategies converge, what kinds of stable patterns (equilibria) emerge, and how these limiting cases can provide deeper insights into the nature of statistical decision-making under uncertainty.


## Unification Through Relative Risk Aversion

A concept of “Statistical Game” is introduced. Frequentist Approach: Focuses purely on frequencies of observed data/outcomes.  Bayesian Approach: Explicitly incorporates prior probability distribution, updated by data. Skipping all the complex mathematical expressions in the paper, I have tried to explain the main intuition of the statistical Game proposed in the paper below:

In this generalized statistical game:

- There are two players
  - Player 1 bets on scenarios chosen by Player 2
- Player 2 picks between two scenarios (A or B) and generates data reflecting that choice
- Player 1 sees some of the data, makes probabilistic guesses about which scenario was picked based on the data, and bets

A key component is Player 1 has a "risk aversion" parameter γ that controls how much they hedge their bets. 

- When γ is small, Player 1 bets aggressively like a frequentist - caring only about the frequencies of data, not any prior belief. 
- As γ increases, they become more Bayesian - weighting prior probabilities more, carefully hedging bets.
- γ can be interpreted as how brave (γ low) vs anxious (γ high) the player is.

The paper shows that the same generalized statistical game framework and math can model both frequentist and Bayesian reasoning just by tuning this one risk aversion parameter γ.

The generalized game helps unify the concepts, showing the only difference is in the agent's willingness to take risks. The proposed Statistical Game paradigm and its analysis of player strategies based on risk preferences provide a novel perspective on integrating theories of decision making under uncertainty.




