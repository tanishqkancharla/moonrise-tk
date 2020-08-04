# The concept of symmetry in Artificial Intelligence

The concept of symmetry is very important in physics. Specifically, the idea that the laws of physics are invariant across space and time. A similar idea is true of our visual understanding. When we see a dog, it doesn't matter where in our visual perception we notice it, we will always classify it as a dog. At the very least, there is radial symmetry in our confidence of an object (as we get further from the center of our vision, we're less sure about the identification of the object).

This sort of "symmetry" is missing from Artificial intelligence. Generally speaking, a prediction on an object will not be radially symmetrical (so the confidence value changes as you go around the circle). 

I think this stems from the lack of understanding of physical principles. To us, we understand object permanence; the idea that an object is intrinsically the same whether it's flipped, rotated, etc. I don't think that sort of understanding is built into machine learning; their notion of symmetry is based on the exact orientation of the training images given to them.

To properly account for this, you would need the model to either be seen every single possible rotation/translation of the object (which is impossible) or somehow get the model to disregard the notion of rotation or translation of the object (since the object's classification does not depend on those two properties). This is related to how for machines, classification is *easier* than object detection:

[[In AI, classification comes before object detection]]