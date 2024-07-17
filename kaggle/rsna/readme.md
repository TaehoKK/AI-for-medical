# 캐글 주소
- https://www.kaggle.com/competitions/rsna-2024-lumbar-spine-degenerative-classification

# pydicom github
- https://github.com/pydicom/pydicom

# Files
### train.csv: Labels for the train set.

- study_id - The study ID. Each study may include multiple series of images.
- [condition]_[level] - The target labels, such as spinal_canal_stenosis_l1_l2, with the severity levels of Normal/Mild, Moderate, or Severe. Some entries have incomplete labels.

### train_label_coordinates.csv

- study_id
- series_id - The imagery series ID.
- instance_number - The image's order number within the 3D stack.
- condition - There are three core conditions: spinal canal stenosis, neural_foraminal_narrowing, and subarticular_stenosis. The latter two are considered for each side of the spine.
- level - The relevant vertebrae, such as l3_l4
- [x/y] - The x/y coordinates for the center of the area that defined the label.

### sample_submission.csv

- row_id - A slug of the study ID, condition, and level such as 12345_spinal_canal_stenosis_l3_l4.
- [normal_mild/moderate/severe] - The three prediction columns.
- [train/test]_images/[study_id]/[series_id]/[instance_number].dcm The imagery data.

### [train/test]_series_descriptions.csv
- study_id
- series_id
- series_description The scan's orientation.
