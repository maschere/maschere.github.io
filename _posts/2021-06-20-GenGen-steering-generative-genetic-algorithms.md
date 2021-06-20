---
title: "GenGen: Steering Generative Genetic Algorithms"
---
## GenGen: Steering Generative Genetic Algorithms
![gengengif](/imgs/gengen.gif "gengengif")

---

[Genetic algorithms](https://www.youtube.com/watch?v=kHyNqSnzP8Y) are "creative" by design, as they explore their respective fitness-function landscape in a randomized, pseudo-evolutionary manner. Hence defining mutation and cross-over processes in a way that allows them to literally paint a picture results in a large variety of images.

To evaluate the fitness -- that is deciding if the picture of one individuum fulfills certain criteria -- requires human judgment in the optimal case. However by letting a pre-trained neural network take on the role of judge, this processes can be steered autonomously and independently of human input. 

Depending on the actual painting capabilities on the individuum, this process does not generate highly realistic examples of the target class. Rather it produces adversarial examples that look like the target class to the neural network, but most likely not to the human eye. Visually pleasing results can be obtained nevertheless. Have a look.

Starting with a blank image:
<video width="400" height="400" controls autoplay muted loop>
  <source type="video/mp4" src="/videos/genGen1.mp4">
</video>

Another variation:
<video width="400" height="400" controls autoplay muted loop>
  <source type="video/mp4" src="/videos/genGen1.mp4">
</video>

Starting with random [Bob Ross](https://github.com/jwilber/Bob_Ross_Paintings) images:
<video width="400" height="400" controls autoplay muted loop>
  <source type="video/mp4" src="/videos/ross.mp4">
</video>

Source code in the form of a Colab notebook is available at https://github.com/maschere/public-jupyter/blob/master/genGen.ipynb
