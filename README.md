This repository allows you to create visualisations of the features found by a sparse autoencoder, like the one below (link [here](https://www.perfectlynormal.co.uk/blog-sae)).

<img src="https://raw.githubusercontent.com/callummcdougall/computational-thread-art/master/example_images/misc/image_sae.png" width="900">

This particular feature seems to be a fuzzy skip trigram, with the pattern being `(django syntax)`, ..., ` ('` -> `django`. You can confirm this by taking some of the text in the top activations that comes immediately before the bracket (e.g. `created_on` or `first_name`), copying it into GPT4 and asking it to identify which library is being used - it will correctly identify these as instances of Django syntax. Furthermore, we can see that this feature boosts `django` a lot more than any other token.

These visualisations were created using the GELU-1l model from Neel Nanda's HuggingFace library, as well as an autoencoder which he trained on its single layer of neuron activations (see [this Colab](https://colab.research.google.com/drive/1u8larhpxy8w4mMsJiSBddNOzFGj7_RTn) from Neel).

You can use my [Colab](https://colab.research.google.com/drive/12Pr0F5ZSTUk65PBgjqNjy0vuyKrvbDty#scrollTo=0Js1mtcXd2LU) to generate more of these visualisations. You can use this [sae visualiser](https://www.perfectlynormal.co.uk/blog-sae) to navigate through the first thousand features of the aforementioned autoencoder.
