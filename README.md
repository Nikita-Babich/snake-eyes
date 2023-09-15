# Write-up for the Snake Eyes prediction market on Manifold Markets


## Introduction

The market creator made around 35 updates to the description of the market. All updates are an attempt to propose a specific method for solution of the problem, but impartial market creator is not supposed to restrict to only one method (incorrect one), if he truly seeks for truth.
In the Description of the market I omitted the part which contains candidate write-ups and links to related markets.

### Header of the question

### Description of the question
You're offered a gamble where a pair of six-sided dice are rolled and unless they come up snake eyes you get a bajillion dollars. If they do come up snake eyes, you're devoured by snakes.

So far it sounds like you have a 1/36 chance of dying, right?

Now the twist. First, I gather up an unlimited number of people willing to play the game. I take 1 person from that pool and let them play. Then I take 2 people and have them play together, where they share a dice roll and either get the bajillion dollars each or both get devoured. Then I do the same with 4 people, and then 8, 16, and so on.

At some point one of those groups will be devoured by snakes and then I stop.

Is the probability that you'll die, given that you're chosen to play, still 1/36?

Argument for NO
Due to the doubling, the final group of people that die is slightly bigger than all the surviving groups put together. So if you're chosen to play you have about a 50% chance of dying! 😬 🐍 

Argument for YES
The dice rolls are independent and whenever you're chosen, whatever happened in earlier rounds is irrelevant. Your chances of death are the chances of snake eyes on your round: 1/36. 😅

Clarifications and FAQ
1. The game is not adversarial and the dice rolls are independent and truly random.
1. Choosing each group also happens uniformly randomly and without replacement.
1. The question is about the unrealistic case of an unbounded number of people but we can cap it and say that if no one has died after N rounds then the game ends and no one dies. We just need to then find the limit as N goes to infinity, in which case the probability that no one dies goes to zero. [ANTI-EDIT: This is back to its original form since a couple people had concerns about whether my attempts to clarify actually changed the question. A previous edit called the answer "technically undefined" in the infinite case, which I still believe is true. The other edit removed the part about how the probability of no one dying goes to zero. That was because I noticed it was redundant with item 5 below.]
1. We're asking for a conditional probability: given that you're chosen to play, what is the probability that you die? I.e., what fraction of people chosen to play die [in expectation]?
1. Importantly, in the finite version it's possible for no one to die. But the probability of that approaches zero as the size of the pool approaches infinity.
1. What if "the fraction of people chosen to play who die in expectation" is different from the conditional probability? Answer: we're talking about the conditional probability. We're treating this as a decision theory problem: assuming you want to play the one-shot version, do you still want to play the doubling-groups version?
1. What if the most correct answer is "undefined"? If we went by just the title of this market, that would be NO, but from the beginning we clarified that NO requires the probability to be strictly greater than 1/36, which "undefined" is not. I failed to consider the possible answer of "undefined" when creating this market! So if that's the answer it's going to be hard to have a satisfactory resolution but I think N/A will be the least unsatisfactory in that case.
1. "At some point one of those groups will be devoured by snakes and then I stop" has an implicit "unless I roll non-snake-eyes forever". I.e., we are not conditioning on the game ending with snake eyes. The probability of an infinite sequences of non-snake-eyes is zero and that's the sense in which it's correct to say "at some point snake eyes will happen" but non-snake-eyes forever is possible in the technical sense of "possible".
1. Via David Pennock: The word "given" is being used in the sense of standard conditional probability: what is the probability that you die in the case where you happen, by random chance, to be chosen. "Given" here does not mean being somehow forced to be chosen. (Corollary: The probability of being chosen is zero in the infinite population case.)

(FAQs 6-9 were added as clarifications based on questions in the comments. Holler if any feel unfair!)

PS: To expand on FAQ8, "probability zero" and "impossible" are mathematically distinct concepts. For example, consider flipping a coin an infinite number of times. Every infinite sequence like HHTHTTHHHTHT... is a possible outcome but each one has probability zero.

Resolution criteria
For an official resolution we'll write up a proof (or "proof") that the answer is 1/36 and a proof that the answer is ~1/2 (really anything greater than 1/36 would be fine) and then recruit some mathematician(s) to make an independent judgment on which is correct. Or maybe we'll just reach consensus in the comments?

## Solution

### Program

## Mistakes of the opposing side

