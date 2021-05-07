---
layout: post
title: xT derivation
---

## Deriving xT
This really short tutorial is meant to provide a really simplistic mathematical explanation and derivation of xT. Please check out Karun's post for more details!

First, assume the player is in possession with the ball at a position x,y on the pitch. The expected threat value at that position is $$xT_{x,y}$$. He has 2 options on the ball – move or shoot. Movement includes passing to a teammate or dribbling while shooting is self explanatory. 

### Shooting
The shooting element of xT is a form of the xG model. I will not be detailing the derivation of xG as this is heavily dependent on the model. For simplicity, xG represented in this section is $$g_{x,y}$$. Here, we introduce a probability $$s_{x,y}$$ which describes the probability of shooting from that position. We get the formula :

$$s_{x,y} \times g_{x,y}$$

### Moving
When moving the ball, the player must decide which of the other 95 zones to move to. Assuming the new zone has coordinates z,w, the new expected threat value will be $$xT_{z,w}$$ at this zone. Here, a transition matrix $$T_{x,y}$$ is introduced.  This transition matrix is derived from past data and describes the payoffs from moving the ball to the new coordinate z,w. In simpler terms, they describe the probability of shifting the ball to this position. Now with this, we can calculate the total payoff for moving the ball but summing it across all zones.

$$
\begin{align*}
  & m_{x,y} \times \sum_{z=1}^{12} \sum_{w=1}^{8}T_{(x,y)\rightarrow (z,w)} \times xT_{z,w}\
\end{align*}
$$

 Now, to combine both the shooting and movement elements of xT, we introduce 2 more probabilities – $$s_{x,y}$$ which describes the probability of shooting from the location and $$m_{x,y}$$ which is the probability of moving the ball. Combining them together, we get:

 $$xT_{x,y} = (s_{x,y} \times g_{x,y}) + (m_{x,y} \times \sum_{z=1}^{12} \sum_{w=1}^{8}T_{(x,y)\rightarrow (z,w)} \times xT_{z,w})\$$

The above formula looks seemingly impossible to solve at first as we do not know what are the values of $$xT$$. Fortunately, there is a way to overcome this by setting $$xT_{x,y}$$ = 0 at an intial position and then solving them iteratively until the values converge.
