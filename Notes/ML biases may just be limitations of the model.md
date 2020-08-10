# ML biases may just be limitations of the model

[https://twitter.com/AlexTamkin/status/1287147874162270214?s=20](https://twitter.com/AlexTamkin/status/1287147874162270214?s=20)

I was looking at this tweet ^ and I responded to it asking why the observed behavior was considered bias. I would first read the above thread I started with the people, but the point I was trying to make was biases in ML models such as automatically assigning a bucket named "Suhail" to India arise from the limitations of the model. Being very trained, GPT-3 knows (correctly) there is some sort of relationship between Suhail and India. So when it assigns a bucket location to India because it's called Suhail, that comes from "oh there is some relationship between the name Suhail and India"

It doesn't understand the nature of this relationship the same way we humans do though. I, for example, know that Suhail is a common Indian name. But if asked to do the same thing GPT-3 was above, I can understand the **name** of the bucket has *no relationship* to **where** it's being assigned to.

GPT-3 doesn't understand that, all it "knows" is there is some association. So when this sort of behavior is called "bias" it doesn't make sense to me, since it's assigning the location just based on whatever association it has stored between Suhail and India. By that logic, I'm biased because I know Suhail is a common Indian name.

Which is actually a reasonable stance to take; I do associate Suhail with India, just like the model does. The difference is, I can understand where that relationship matters and where it doesn't. Above, the name Suhail is just a placeholder but if I was asked instead to predict which country the name Suhail is most common in, I would answer India (correctly, I think). However if I was just asked to make an aws bucket with the name Suhail, then I would either ask for the location or have some default I use.

So my stance is the model knows there is some relationship between Suhail and India. Calling it bias is confusing, because it makes it sound like it's undesirable behavior. In reality we'd probably want the model to understand there is a relationship between the two but understand where it matters and where it doesn't.

Anyway this is my opinion. There might be something else here I'm missing.