# justmarried
## A graph theory approach to marriage, roommates, and college.
This project is concerned with matching people to people and people to things. Two problems of matching people are explored. The first comes up when trying to arrange marriages. This would be an easy problem if no one had preferences that overlapped. But the real world doesn't care if problems are easy. So rather than trying to arrange marriages that are simultaneously optimal for everyone, this solution finds an arrangment where no two people would want to be married to eachother more than their current spouse. 

### Marriage
Imagine this scenario: 
> A town would like to arrange marriages for its single men and women. Each person has a list of opposite sex suitors in order of preference. The town would like to find an arrangement that ensures no two people would rather be with eachother than with their partner. In other words, marriages should be stable. 

This is called the stable marriage problem (or the stable matching problem), which this project explores in detail. In addition, it will dive into two variations of stable matching, namely the stable roommates problem and the college admissions problem (also known as the hospital/residents problem).

Lloyd Shapely and David Gale were awarded the Nobel Prize in 1962 for proving that [for any pattern of preferences, it is always possible to find a set of stable marriages](https://apps.dtic.mil/dtic/tr/fulltext/u2/251958.pdf). They proved that there's always a configuration where instability doesn't occur. (Instability is when two people prefer each other over their partners.) The walkthrough below will make some sense of this.

The Gale-Shapely algorithm has the [following steps](https://www.youtube.com/watch?v=Qcv1IqHWAzg):
1. Everyone creates a list of who they'd like to marry in order of preference.
1. On day one, women submit their proposals to the men. Some men won't receive any, while others will receive more than one. Men that receive a proposal select the person they most prefer.
1. On day two, women that were rejected submit a proposal to their next choice. Men can negate their previous agreement if they receive a better proposal.
1. This continues for days three, four, five, etc.
1. Finally, a configuration is reached where everyone is in a stable marriage.

The  algorithm consists of [the following theorems](https://www.youtube.com/watch?v=LtTV6rIxhdo)::
* *Theorem 0* It eventually stops.
* *Theorem 1* It finds stable marriages.
  * Proof: No woman can trade since they propose their next highest preference each day until they're no longer rejected.
* *Theorem 2* It assigns every woman her best possible husband.
* *Theorem 3* It assigns every man his worst possible wife.

This algorithm arranges [simultaneously optimal marriages for women and simultaneously suboptimal marriages for men](https://youtu.be/LtTV6rIxhdo?t=331), leading to an interesting property; **It's far better to propose than to be proposed to!**

### Roommates

### College
