# Models
Models yang dihasilkan setelah proses machine learning development

## Model Hairloss
Contoh Input
    "stay_up_late": 3,
    "coffee_consumed": 1,
    "brain_working_duration": 0,
    "pressure_level": 0,
    "stress_level": 0,
    "swimming": 1,
    "hair_washing": 1,
    "dandruff": 0

Output Model
[[3.4500108e-08, 9.9999726e-01, 2.6979098e-06, 4.6054815e-08]]

Dari output model, diambil nilai max. Pada contoh di atas, adalah 9.9999726e-01 pada index 1.
Mapping label:
  Index 0 : Normal
  Index 1 : Slight Hair Loss
  Index 2 : Hair Loss
  Index 3 : Serious Hair Loss

Output Tampilan
Slight Hair Loss
0.9999972581863403
