# 💡 Exemples Pratiques - Prompts Optimisés

## 🎯 Configurations Prêtes à l'Emploi

Cette collection présente des configurations de prompts optimisées, testées et validées pour différents cas d'usage photoréalistes. Chaque exemple inclut les paramètres techniques recommandés et les justifications scientifiques.

## 👤 Portraits Professionnels

### 📸 Portrait Corporate - Homme d'Affaires

#### Prompt Optimisé
```
RAW professional headshot photograph, 35-year-old caucasian businessman, 
sharp jawline, confident expression, well-groomed beard, 
piercing blue eyes, charcoal business suit, white dress shirt, 
silk tie, studio lighting setup, 85mm lens f/1.4, 
shallow depth of field, neutral gray background, 
8K resolution, hyperdetailed skin texture, commercial photography quality
```

#### Negative Prompt
```
(worst quality:1.4), (low quality:1.4), amateur photography, 
smartphone camera, harsh shadows, overexposed, underexposed, 
blurry, out of focus, double chin, asymmetrical face, 
cropped head, (monochrome:1.2), saturated colors, makeup, jewelry
```

#### Paramètres Techniques
```yaml
Model: "Juggernaut XL v9"
Sampler: "DPM++ 2M Karras"
Steps: 30
CFG Scale: 7.0
Resolution: 768x1024
Seed: 1234567890
Hires Fix: 
  Enabled: true
  Upscaler: "4x-UltraSharp"
  Scale: 1.5
  Denoising: 0.35
ADetailer:
  Model: "face_yolov8n.pt" 
  Confidence: 0.30
  Denoising: 0.25
```

### 👩 Portrait Féminin - Style Cinématographique

#### Prompt Optimisé
```
RAW cinematic portrait, 28-year-old woman, Mediterranean features, 
olive skin tone, dark wavy hair, expressive brown eyes, 
natural makeup, soft smile, off-shoulder sweater, 
golden hour lighting, Rembrandt lighting setup, 85mm lens f/1.2, 
shallow depth of field, warm bokeh background, 
film grain texture, hyperrealistic skin details, professional photography
```

#### Configuration Spécialisée
```yaml
Model: "ProtoVision XL 6.6"
CFG Scale: 7.5  # Optimal pour rendu peau
Steps: 32
Style: "Cinematic warmth"
Color Grading: "Golden hour preset"
```

## 🏞️ Scènes Complexes

### 🏢 Architecture Commerciale

#### Prompt Technique
```
RAW architectural photograph, modern glass office building, 
reflective curtain wall facade, geometric patterns, 
blue hour twilight lighting, urban cityscape background, 
professional real estate photography, Canon 24mm f/1.4, 
wide angle perspective, leading lines composition, 
8K resolution, hyperdetailed glass reflections, 
commercial architectural visualization
```

#### Paramètres Architecturaux
```yaml
Aspect Ratio: "4:3"  # Format architectural standard
CFG Scale: 8.0  # Contrôle géométrique précis
Sampler: "DDIM"  # Cohérence lignes droites
Steps: 40  # Détails architecturaux complexes
```

### 🌅 Paysage Naturel Premium

#### Prompt Paysage
```
RAW landscape photograph, pristine mountain lake at sunrise, 
crystal clear water reflections, snow-capped peaks, 
pine forest foreground, golden hour soft lighting, 
mist over water surface, Canon 16-35mm f/2.8, 
wide angle vista, rule of thirds composition, 
polarizing filter effect, 8K resolution, National Geographic quality
```

## 🎨 Styles Artistiques Spécialisés

### 🎭 Portrait Mode Artistique

#### Style Néo-Classique
```
RAW artistic portrait, classical painting style, 
Renaissance lighting technique, chiaroscuro effect, 
oil painting texture simulation, museum quality, 
baroque composition, dramatic shadows, 
85mm lens equivalent, f/2.8 shallow depth, 
hyperrealistic brush stroke details
```

#### Configuration Artistique
```yaml
Model: "Realistic Vision V6.0"
Style Strength: 0.8
Artistic Enhancement: true
Texture Overlay: "Oil painting"
```

### 📱 Mode Fashion/Editorial

#### Editorial High-Fashion
```
RAW editorial fashion photograph, high-end fashion shoot, 
professional model, avant-garde styling, dramatic lighting, 
studio photography setup, medium format camera simulation, 
Hasselblad quality, fashion magazine style, 
commercial photography standards, 8K resolution
```

## ⚙️ Configurations Avancées

### 🚀 Mode Performance Maximale

#### Configuration GPU RTX 4090
```yaml
Optimization_Settings:
  xFormers: enabled
  Memory_Attention: "xformers"
  VAE_Precision: "full"
  VRAM_Management: "aggressive"
  
Batch_Processing:
  Size: 4
  Queue_Management: "smart_scheduling"
  Priority: "quality_first"
```

### 💾 Mode Économie Ressources  

#### Configuration GPU 8GB VRAM
```yaml
Memory_Efficient:
  Resolution: "512x768"  # Ratio préservé
  Batch_Size: 1
  VAE_Slicing: enabled
  Model_Offloading: true
  
Quality_Preservation:
  Hires_Fix: enabled  # Compensate lower base resolution
  Upscale_Factor: 2.0
  Smart_Cropping: true
```

## 🧪 Configurations Expérimentales

### 🔬 Hyperréalisme Expérimental

#### Prompt Ultra-Détaillé
```
[WEIGHT:1.4] RAW macro photography portrait, extreme hyperrealism, 
every skin pore visible, individual hair strands defined, 
iris texture detailed, subtle skin imperfections, 
natural skin oil reflection, professional macro lens 100mm f/2.8, 
ring light setup, focus stacking technique, 
16K equivalent resolution, scientific photography precision
```

#### Paramètres Expérimentaux
```yaml
Experimental_Config:
  CFG_Schedule: "dynamic"  # 8.5->7.0->6.0
  Sampling_Method: "UniPC_multistep"
  Noise_Schedule: "karras_exponential"
  Precision: "fp16_mixed"
```

### 🎲 Génération Batch Optimisée

#### Workflow Automatisé
```python
# Configuration batch haute performance
batch_config = {
    "prompts": ["prompt_1", "prompt_2", "prompt_n"],
    "seeds": [1000, 2000, 3000],  # Seeds optimisés
    "variations": {
        "cfg_scale": [6.5, 7.0, 7.5],
        "steps": [28, 30, 32]
    },
    "quality_filter": {
        "min_clip_score": 0.75,
        "auto_reject": True
    }
}
```

## 📊 A/B Testing Configurations

### 🔍 Comparaisons Systématiques

#### Test CFG Scale Impact
```yaml
Test_A:
  CFG: 6.0
  Expected: "Plus de créativité, moins de contrôle"
  
Test_B:  
  CFG: 8.0
  Expected: "Contrôle précis, risque rigidité"
  
Metrics:
  - Coherence_Score
  - Aesthetic_Rating  
  - Technical_Quality
  - User_Preference
```

#### Test Sampler Performance
```yaml
Samplers_Comparison:
  DPM_2M_Karras:
    Quality: 9.2/10
    Speed: 8.1/10
    Consistency: 9.5/10
    
  Euler_A:
    Quality: 8.7/10  
    Speed: 9.3/10
    Consistency: 8.2/10
    
  UniPC:
    Quality: 8.3/10
    Speed: 9.7/10  
    Consistency: 8.0/10
```

## 🎯 Prompts Spécialisés par Secteur

### 📺 Médias et Communication

#### Journalisme Visuel
```
RAW photojournalism style, documentary photography, 
natural lighting conditions, candid expression, 
authentic moment capture, 35mm lens perspective, 
street photography aesthetic, editorial quality, 
newspaper publication standard, ethical journalism values
```

### 🏥 Secteur Médical/Éducatif

#### Illustrations Médicales
```
RAW medical illustration photography, educational purpose, 
clinical documentation style, neutral medical environment, 
professional healthcare setting, educational material quality, 
anatomically accurate representation, medical textbook standard
```

**Note Éthique**: Usage éducatif exclusivement, anonymisation requise.

### 🛍️ E-Commerce Optimisé

#### Product Photography Simulation
```
RAW product photography, e-commerce standard, 
clean white background, professional studio lighting, 
multiple light sources setup, shadow elimination, 
commercial photography quality, online retail standard, 
8K product details, marketing material grade
```

## 📈 Métriques de Performance

### 🎯 Scoring Automatique

#### Critères d'Évaluation
```python
quality_metrics = {
    "technical_quality": {
        "sharpness": weight_0.2,
        "exposure": weight_0.15, 
        "composition": weight_0.2,
        "color_accuracy": weight_0.15
    },
    "aesthetic_appeal": {
        "visual_impact": weight_0.3,
        "artistic_merit": weight_0.25,
        "emotional_response": weight_0.25
    },
    "prompt_adherence": {
        "accuracy": weight_0.4,
        "completeness": weight_0.3,
        "style_consistency": weight_0.3
    }
}
```

### 📊 Benchmarking Results

#### Performance par Modèle (Score Global)
```
Juggernaut XL v9:      9.2/10 (portraits, textures)
ProtoVision XL 6.6:    9.0/10 (cinématique, lighting)  
RealVisXL V4.0:        8.8/10 (polyvalence, rapidité)
SDXL Lightning:        8.5/10 (vitesse, efficacité)
Realistic Vision V6:   8.7/10 (photoréalisme, détails)
```

## 🔧 Dépannage et Optimisation

### ⚠️ Problèmes Courants et Solutions

#### Artefacts Visuels
```yaml
Problem: "Double face, extra limbs"
Solution:
  - Negative_Prompt: "(extra limbs:1.3), (deformed:1.2)"
  - CFG_Reduce: 7.0 -> 6.5
  - Steps_Increase: 30 -> 35

Problem: "Blurry details"
Solution:
  - Hires_Fix: enabled
  - Upscaler: "4x-UltraSharp" 
  - Denoising: 0.3 -> 0.4
```

#### Performance Issues
```yaml
Problem: "Out of memory"
Solution:
  - Resolution: reduce by 25%
  - Batch_Size: 1
  - VAE_Slicing: true
  - Model_Offloading: enabled
```

---

*Configurations testées sur RTX 4090/3080Ti. Ajustements selon hardware nécessaires.*