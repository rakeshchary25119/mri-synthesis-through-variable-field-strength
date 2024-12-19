
# **MRI Synthesis Through Variable Field Strength**

## **Overview**  
This project explores how varying magnetic field strengths (0.5T to 9T) influence MRI imaging parameters such as contrast, sharpness, noise, and signal-to-noise ratio (SNR). By leveraging the **OASIS dataset**, we simulate and analyze MRI images using physics-driven models for T1- and T2*-weighted imaging. Our work aims to provide insights into optimizing imaging protocols for improved clarity, contrast, and diagnostic accuracy.

---

## **Key Features**  

### **1. Data Preparation**  
- Processed segmented tissue maps for White Matter, Gray Matter, and Cerebrospinal Fluid in NIfTI format.  
- Used tools like **NiBabel** to handle neuroimaging data and ensured consistent analysis by selecting a representative axial slice.  

### **2. MRI Signal Modeling**  
- Calculated **relaxation times (T1, T2*) as functions of magnetic field strength.  
- Determined **optimal echo time (TE)** and **flip angles** to maximize tissue contrast.  
- Simulated and analyzed **SNR trends** across magnetic field strengths, highlighting tissue-specific resilience.  

### **3. Noise Simulation**  
- Introduced Gaussian noise to emulate real-world MRI challenges.  
- Analyzed how noise impacts tissues at different field strengths and identified trade-offs in imaging clarity and SNR.  

### **4. Resolution Variations**  
- Simulated varying slice thicknesses (1mm–10mm) and in-plane resolutions (1mm x 1mm to 2mm x 2mm).  
- Observed the effects on sharpness, Root Mean Square Error (RMSE), and tissue differentiation.  

### **5. Advanced Metrics Analysis**  
- Employed **Gradient Entropy (gEn)** to quantify image texture and noise.  
- Modeled sharpness to evaluate boundary delineation between tissues like CSF and White Matter.  

---

## **Repository Contents**  

1. **`Data/`**: Contains the processed NIfTI files used for simulation.  
2. **`Scripts/`**: Python scripts implementing:
   - Data preparation
   - MRI signal modeling
   - Noise simulation
   - Resolution adjustments  
3. **`Docs/`**: Comprehensive report detailing methodology, results, and insights.  

---

## **Getting Started**  

### **Prerequisites**  
- Python 3.8+  
- Libraries: `numpy`, `scipy`, `matplotlib`, `nibabel`, `pandas` 

### **Setup**  
1. Clone this repository:  
   ```bash
   git clone https://github.com/rakeshchary25119/mri-synthesis-through-variable-field-strength.git
   cd mri-synthesis-through-variable-field-strength 
   ```  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```  
3. Run the scripts to replicate simulations or analyze results.  

---

## **Usage**  

### Simulating MRI Images  
Use the provided Python scripts to:
1. Generate synthetic T1- and T2*-weighted images for specified magnetic field strengths.  
2. Add Gaussian noise and analyze its impact on imaging parameters.  
3. Adjust slice thickness and in-plane resolution to study resolution effects.  

### Visualization  
- View generated SNR maps, sharpness graphs, and image quality comparisons under different field strengths and resolutions.  

---

## **Results**  

Key insights from the project include:
- **SNR Trends**: White Matter exhibits higher resilience to noise at higher magnetic field strengths.  
- **Resolution Effects**: Finer resolutions improve tissue differentiation but may increase noise sensitivity.  
- **Noise Impact**: Higher magnetic fields improve SNR but amplify noise, requiring careful imaging protocol adjustments.  

---

## **Acknowledgments**  
This project was guided by **Professor Nikolaos Tsekos** and supported by **Javadi Mohammad** and **Murphy Michael P**, whose mentorship was invaluable.  

---

## **Contributions**  
We welcome contributions to enhance this project. Please feel free to fork the repository, create feature branches, and submit pull requests.  
