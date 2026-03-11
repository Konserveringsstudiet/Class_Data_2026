# Colourimetry Data
The measurements of colour in 11 paint samples is shown in this dataset. The samples have been painted with a madder lake and was then placed in a windowsill for approximately 2 months. Each sample was divided into three sections: one left uncovered, the second covered with a UV-filtering acrylic (TruVue Optium Museum Acrylic, UV 99%, referred to as TruVue in the data), and the third entirely covered. Each section of each sample had five colour measurements taken on different places to create a varied sample size.

## Instrument & Data Processing
A Konica Minolta CM 700d spectrophotometer with a 3 mm opening. It has a Xenon lamp and an 8º detector reflection angle in spectacular component (SCE) mode. The measurements are expressed in the CIELAB (Commission Internationale de l’Eclairage) colour system, which is separated into L*, a*, and b* values. L* is the brightness of the colour, where an increasing number expresses a darker colour (100 = 100 black). A* indicates the hue on a spectrum between red and green, and b* indicates the colour on the spectrum between blue and yellow. These expresses the coordinates of the sample colour within the CIELAB colour map. In addition to the raw data, some of the processed data used in the project is also included; these are E, ΔE, and the averages. The E has been calculated as the squared sum of the LAB values. It was in this project used to transform each measurement into a single value for Analysis of Variance (ANOVA) testing.

ΔE was also calcluated for each sample in order to understand the differences between the uncovered, TruVue, and covered sections. It is the distance between two points in the 3D colour space, and indicates here how significant the overall change in colour in two comparative samples are. Finally, the average was calculated as the sum of the L*, a* and b* values separately for each section, divided by the number of values in the dataset.

## Data Dictionary 

### Colourimetry Data

|  **_Field Name_**  | **_Data Types_** | **_Missing Values_** | **_Description_** | **_Example_** | **_Notes_** | 
|:------------------:|:----------------:|:--------------------:|:-----------------:|:-------------:|:-----------:|
| _Paint Mixture_ | alphabetical | n/a | The paint mixture used to create the sample. | A | Two mixtures created at different times without set mixing ratios. |
| _Sample_ | numerical | n/a | An individual sample as seen in "Images all samples". | 3 | Samples have the same number in both survey and colourimetry data. | 
| _Uncovered L*_ | numerical | n/a | The value indicating the brightness of the uncovered section. | 40,31 | In L* values, the higher the number is the darker the colour is, with 100 being perfect black. | 
| _Uncovered a*_ | numerical |	n/a | The value of the colour hue on a spectrum between red and green, on the uncovered section of each sample. | 47,06 | |
| _Uncovered b*_ | numerical |	n/a | The value of the colour hue on a spectrum between blue and yellow, on the uncovered section of each sample. | 29,66 | |
| _TruVue L*_ | numerical |	n/a | The value indicating the brightness of the TruVue UV filter covered section. | 37,46 | In L* values, the higher the number is the darker the colour is, with 100 being perfect black.| 
| _TruVue a*_ | numerical |	n/a | The value of the colour hue on a spectrum between red and green, on the TruVue UV filter covered section of each sample. | 50,21 | 
| _TruVue b*_ | numerical |	n/a | The value of the colour hue on a spectrum between blue and yellow, on the TruVue UV filter covered section of each sample. | 26,5 | 
| _Covered L*_ | numerical |	n/a | The value indicating the brightness of the covered section. | 33,98 | In L* values, the higher the number is the darker the colour is, with 100 being perfect black. | 
| _Covered a*_ | numerical |	n/a | The value of the colour hue on a spectrum between red and green, on the covered section of each sample. | 45,41 | | 
| _Covered b*_ | numerical |	n/a | The value of the colour hue on a spectrum between blue and yellow, on the covered section of each sample. | 28,71 | 
| _E value_ | numerical |	n/a | The squared sum of the L*, a* and b* values for a specific section. | 64,57 | It is calculated as: E=√((L*)^2+(a*)^2+(b*)^2) | 

### DeltaE Data

|  **_Field Name_**  | **_Data Types_** | **_Missing Values_** | **_Description_** | **_Example_** | **_Notes_** | 
|:------------------:|:----------------:|:--------------------:|:-----------------:|:-------------:|:-----------:|
| _ΔE (DeltaE)_ | title | n/a  | The colour difference between two measurements. | | ΔE is calculated as: ΔE*=√((ΔL*)^2+(Δa*)^2+(Δb*)^2) Where ΔL*, Δa*, and Δb* is the L*, a* or b* value of one of the three sections' measurement subtracted by the same value from one of the other three sections. |
| _Covered vs. Uncovered_ | numerical |	n/a | The colour difference (ΔE) between the measurments of the covered and uncovered sections. | 4,6 | | 
| _Covered vs. TruVue_ | numerical |	n/a | The colour difference (ΔE) between the measurments of the covered and TruVue sections. | 1,92 | | 
| _Uncovered vs. TruVue_ | numerical |	n/a | The colour difference (ΔE) between the measurments of the uncovered and TruVue sections. | 2,78 | | 
