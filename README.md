# Image Generation Task Repository

Welcome to the repository documenting various image generation approaches and the outcomes achieved in our exploration. This project focuses on using advanced Stable Diffusion (SD) and ControlNet methods for generating customized images of Character Skins of various characters from the game: Clash of Clans.

---

## Approaches Explored:

1. **Stable Diffusion (SD) + ControlNet**
2. **Finetuning Pretrained SD on Custom Dataset**
3. **Finetuned SD + ControlNet**
4. **Textual Inversion**

---

### 1. **SD + ControlNet**

We started with the basic approach of combining **Stable Diffusion (SD)** and **ControlNet**. Specifically, we utilized the `CompVis SD-v1-4` model with `lllyasviel control_v11p_sd15_inpaint` ControlNet to tackle the image generation task. Here we utilzed the `mattmdjaga/segformer_b2_clothes` for mask generation

#### Results:

- **Input:**  
  ![Input Image](https://github.com/user-attachments/assets/e7f92ac0-5046-4157-9e56-6fe731fe4565)

- **Mask:**  
  ![Mask Image](https://github.com/user-attachments/assets/9210f21f-5d0d-401b-a90e-f9951897d736)

- **Output:**  
  ![Output 1](https://github.com/user-attachments/assets/704a75d1-4fca-47d8-95d2-3605d729cabf)  
  ![Output 2](https://github.com/user-attachments/assets/c1637723-63f0-4f1d-b063-17f0c1b6243d)

---

### 2. **Finetuning Pretrained SD on Custom Dataset**

Next, we decided to finetune the **ControlNet** model on a custom dataset to further refine the results. We used a dataset of **80 images** (resolution: **512x512**) and finetuned the model for **40 steps**. This resulted in clearer and more accurate outputs that adhered to the prompt.
Finetuning photo:
![WhatsApp Image 2024-09-09 at 18 40 17_f4702608](https://github.com/user-attachments/assets/46d6d896-3aa9-4f95-b847-a9c90a888bf4)


---

### 3. **Finetuned SD + ControlNet**

We combined the finetuned SD with ControlNet. 
#### Results:

- **Prompt:** Santa Claus  
- **Output:**  
  ![Santa Claus Output](https://github.com/user-attachments/assets/c6fe535f-eaff-4528-bbc4-a7038bbb91f7)
---

### 4. **Textual Inversion**

We also experimented with **Textual Inversion** on  `CompVis SD-v1-4`; however the model relied on CLIP for text encoding, which has a token limit. Thus it was working well for text prompts but not yet functional for image input.

---

For more details and the scripts used in the finetuning process, please refer to the codebase above.
