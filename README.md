# 🧬 Molecular Docking of Phytochemicals Against DNA Gyrase

---

## 📌 Project Description
This project performs **molecular docking analysis** of selected phytochemicals against **DNA Gyrase**, a key bacterial enzyme involved in DNA replication.

Using **AutoDock Vina**, the binding affinity and interaction patterns of compounds were evaluated. The study highlights potential natural inhibitors for antibacterial drug development.

---

## 🎯 Objectives
- Perform molecular docking using AutoDock Vina  
- Compare binding affinities of phytochemicals  
- Identify potential inhibitors of DNA Gyrase  
- Analyze ligand–protein interactions  

---

## 🧪 Ligands Used
- Catechin - Catechin is a natural flavonoid commonly found in green tea and known for its antioxidant properties. Its multiple hydroxyl groups enable strong hydrogen bonding with target proteins, contributing to higher binding affinity in docking studies.
  
 ![Catechin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/ligand/Catechin.png)
- Quercetin - Quercetin is a plant-derived flavonoid with potent antioxidant and anti-inflammatory activity. Its planar structure and hydroxyl-rich composition facilitate stable interactions with protein active sites.
  
![Quercetin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/ligand/Quercetin.png)
- Berberine - Berberine is an isoquinoline alkaloid with known antimicrobial properties. Its aromatic structure allows interactions such as π–π stacking, contributing to moderate binding with target proteins.
  
 ![Berberine](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/ligand/Berberine.png)
- Curcumin - Curcumin is a bioactive compound from turmeric with anti-inflammatory and antioxidant effects. Due to its flexible structure, it shows comparatively weaker and less stable binding in docking studies.
  
  ![Curcumin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/ligand/Curcumin.png)

---

## 🧬 Target Protein
- DNA Gyrase - DNA gyrase is a bacterial enzyme belonging to the topoisomerase II family that introduces negative supercoils into DNA, which is essential for DNA replication and transcription. It plays a critical role in maintaining DNA topology during cellular processes. Due to its unique presence in bacteria, DNA gyrase is a major target for antibacterial drug development.
  
- File used: `clean_protein.pdbqt`
  ![DNA Gyrase](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Protein/gyrase.png)


---

## ⚙️ Tools & Software
- AutoDock Vina  
- PyMOL  
- Open Babel  

---

## 📂 Project Structure
### 📁 Folder Description

- **Protein/** → Contains prepared protein files  
- **Ligands/** → Contains ligand structures  
- **Docking/** → Output files from AutoDock Vina  
- **Results/** → Graphs and interaction images  
- **Scripts/** → Docking commands and scripts
---

---

## ⚙️ Docking Parameters

| Parameter        | Value |
|----------------|------|
| Grid Size       | 20 × 20 × 20 Å |
| Exhaustiveness  | 16 |
| Center (X,Y,Z)  | 19.601, 19.15, 43.344 |

---

## 📊 Binding Energy Comparison

![Binding Graph](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Result/Binding%20Energy%20(kcal_mol)%20vs.%20Compound.png)

---

## 📸 Molecular Interaction Visualizations

### 🔹 Catechin
![Catechin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Result/catechine2.png)

---

### 🔹 Quercetin
![Quercetin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Result/quercetin2.png)

---

### 🔹 Berberine
![Berberine](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Result/berbeqine2.png)

---

### 🔹 Curcumin
![Curcumin](https://github.com/ayushtiwari2105G/DNA_Gyrase_Docking/blob/main/DNA_Gyrase_Docking/Result/curcumine2.png)

---

## 📊 Results

| Compound   | Binding Energy (kcal/mol) | Reason for Binding Affinity |
|------------|--------------------------|-----------------------------|
| Catechin   | -7.914 | High number of hydroxyl (–OH) groups enables strong hydrogen bonding and stable interaction within the binding pocket |
| Quercetin  | -7.687 | Planar flavonoid structure with multiple –OH groups promotes hydrogen bonding and good fit in active site |
| Berberine  | -7.105 | Aromatic structure allows π–π stacking interactions but fewer hydrogen bonds reduce overall affinity |
| Curcumin   | -6.44  | Flexible structure with fewer effective interactions leads to weaker and less stable binding |

---

## 🔬 Key Findings

- Catechin showed the strongest binding affinity  
- Quercetin also demonstrated strong interaction  
- Berberine showed moderate binding  
- Curcumin showed weaker interaction  

---

## 🧠 Conclusion

Catechin and Quercetin exhibit strong inhibitory potential against DNA Gyrase and may serve as promising candidates for antibacterial drug development.

---

## 🚀 How to Run Docking

```bash
vina --receptor Protein/clean_protein.pdbqt \
     --ligand Ligands/catechin.pdbqt \
     --center_x 19.601 \
     --center_y 19.15 \
     --center_z 43.344 \
     --size_x 20 \
     --size_y 20 \
     --size_z 20 \
     --exhaustiveness 16 \
     --out Docking/catechin_out.pdbqt
