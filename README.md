# **Game Character Skin Generation Using Stable Diffusion and ControlNet**

Welcome to the repository showcasing various state-of-the-art image generation approaches tailored for generating game character skins. Our project leverages advanced techniques such as **Stable Diffusion (SD)** and **ControlNet** to generate customized skin variations for characters from the game **Clash of Clans**. 

---

## **Project Overview**

This project focuses on experimenting with different methods to enhance the quality, flexibility, and control over image generation tasks. By fine-tuning pretrained models and leveraging advanced neural network architectures, we aimed to create visually compelling and unique character skins.

---

### **Key Approaches Explored**

1. **Stable Diffusion (SD) + ControlNet**
2. **Finetuning Pretrained SD on a Custom Dataset**
3. **Combining Finetuned SD with ControlNet**
4. **Textual Inversion on SD**

---

### 1. **Stable Diffusion + ControlNet**

Our initial approach involved utilizing **Stable Diffusion** with **ControlNet** to generate character skins. We employed the `CompVis SD-v1-4` model alongside `lllyasviel control_v11p_sd15_inpaint` for image generation, using the `mattmdjaga/segformer_b2_clothes` model to generate masks for character details.

**Pipeline Overview:**
- **Base Model**: CompVis SD-v1-4
- **ControlNet**: Inpainting with lllyasviel ControlNet
- **Mask Generation**: SegFormer B2 for clothing segmentation

**Results:**
- **Input Image**  
  ![Input Image](https://github.com/user-attachments/assets/e7f92ac0-5046-4157-9e56-6fe731fe4565)
  
- **Generated Mask**  
  ![Mask Image](https://github.com/user-attachments/assets/9210f21f-5d0d-401b-a90e-f9951897d736)

- **Outputs**  
  ![Output 1](https://github.com/user-attachments/assets/704a75d1-4fca-47d8-95d2-3605d729cabf)  
  ![Output 2](https://github.com/user-attachments/assets/c1637723-63f0-4f1d-b063-17f0c1b6243d)

---

### 2. **Fine-Tuning Pretrained SD on a Custom Dataset**

To improve generation accuracy, we fine-tuned the SD model on a custom dataset of **80 images** (each at **512x512 resolution**), refining the model's understanding of character features. After **40 training steps**, the model delivered more consistent and precise results.

**Fine-Tuning Configuration:**
- **Dataset**: 80 custom 512x512 images
- **Training Steps**: 40 steps

**Finetuning Result**  
  ![Finetuning Result](https://github.com/user-attachments/assets/46d6d896-3aa9-4f95-b847-a9c90a888bf4)

---

### 3. **Combining Finetuned SD with ControlNet**

This approach combined the finetuned SD model with ControlNet for enhanced image control, enabling specific character skin details to be modified based on prompts. The outputs showed significant improvement in texture and detail precision.

**Sample Prompt:** Santa Claus  
**Output:**  
  ![Santa Claus Output](https://github.com/user-attachments/assets/c6fe535f-eaff-4528-bbc4-a7038bbb91f7)

---

### 4. **Textual Inversion on Stable Diffusion**

We also experimented with **Textual Inversion** on `CompVis SD-v1-4` to create embeddings for unique character skins using text prompts. The approach worked well for generating text-based prompts but encountered limitations when handling detailed image inputs due to the token restrictions of CLIP.

---

### **Conclusion & Future Work**

Our exploration has demonstrated that combining finetuned models with advanced neural architectures like ControlNet significantly improves image generation tasks. Future work will focus on refining Textual Inversion techniques for better image generation and further optimizing model fine-tuning for larger datasets.

For more details and access to the finetuning scripts and evaluation notebooks, explore the repository.

--- 

