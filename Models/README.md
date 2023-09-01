# Models
Models yang dihasilkan setelah proses machine learning development

## Model Hairloss
Contoh Input <br>
- "stay_up_late": 3,
- "coffee_consumed": 1,
- "brain_working_duration": 0,
- "pressure_level": 0,
- "stress_level": 0,
- "swimming": 1,
- "hair_washing": 1,
- "dandruff": 0 <br>

Output Model <br>
[[3.4500108e-08, 9.9999726e-01, 2.6979098e-06, 4.6054815e-08]] <br>

Dari output model, diambil nilai max. Pada contoh di atas, adalah 9.9999726e-01 pada index 1. <br><br>
Mapping label:
  - Index 0 : Normal
  - Index 1 : Slight Hair Loss
  - Index 2 : Hair Loss
  - Index 3 : Serious Hair Loss <br>

Output Tampilan <br>
Slight Hair Loss <br>
0.9999972581863403

## Model Scalp Disease
Contoh Input <br>
- image1: valid <br>

Output Model <br>
[[7.1049097e-04, 3.8028753e-04, 1.4329808e-03, 9.9747437e-01, 1.8849778e-06]] <br>

Dari output model, diambil nilai max. Pada contoh di atas, adalah 9.9747437e-01 pada index 3. <br><br>
Mapping label:
  - Index 0 : alopecia-areata
  - Index 1 : normal
  - Index 2 : scalp-psoriasis
  - Index 3 : seborrhoeic-dermatitis
  - Index 4 : tinea-capitis <br>

Output Tampilan <br>
seborrhoeic-dermatitis <br>
0.99747437
