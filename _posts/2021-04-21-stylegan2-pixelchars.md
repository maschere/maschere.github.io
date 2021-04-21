## Finetuning a [StyleGAN2](https://github.com/NVlabs/stylegan2-ada-pytorch) FFHQ model to a collection of [pixel characters](https://www.kaggle.com/calmness/retro-pixel-characters-generator) and purposely underfitting it sure leads to some interesting results.
![detail crop](/imgs/ganchar/fakes000020detail.jpg "detail crop")

---

I finetuned NVIDIA's FFHQ256 Stylegan2-ada-pytorch model by showing it only about 20.000 instances of 64x64 pixel characters (upsampled to 256x256). This took around 30 minutes on Colab. Here are some more (uncurated) results.

![full img](/imgs/ganchar/fakes000020sm.jpg "full img")
(download a high-res image [here](/imgs/ganchar/fakes000020.jpg))