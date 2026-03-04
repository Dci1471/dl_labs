# Лабораторная работа №1
## Создание модели классификации изображений овощей/фрутов
[Веса моделей](https://drive.google.com/file/d/1VM8KXjRX5b9g2SkU5h_4CIfxyqWaJm3s/view?usp=sharing)
## Описание:
- Архитектура: ансамбль, выбирающий моду из предсказаний 5 дообученных EfficientNet‑B3
- RandomResizeCrop, обрезающий изображение до (224x224)
- 5 fold Cross-Validatiom
- Аугментация (Flips. ColorJitter, GaussNoises, GaussianBlur, Coarse_Dropout)
- Взвешивание классов (compute_class_weight из sklearn) и Label_smoothing
- Оптимизатор AdamW
- Адаптивный LR (ReduceLROnPlateau)
- Batch_Size 64
## Результаты

| model | accuracy |
| --- | --- |
| baseline | 87.2 |
| resnet50, label_smoothing, weights, addaptive_lr, data cleanup | 91.8 |
| augmentation_changes, AdamW, kfold, efficientnet_b3, ensamble_models | 95.2 |
