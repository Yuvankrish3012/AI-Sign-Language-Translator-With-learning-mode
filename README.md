Final Feature List: AI Sign Language Translator
(I) Dataset Handling
Merged multiple sign language datasets:

1. ASL Alphabet Dataset (A-Z, "del", "nothing", "space")
2. Indian Sign Language (ISL) Dataset (Alphabets & Numbers)
3. LSA64 Dataset (Argentinian Sign Language - 64 Signs)
4. Mendeley Dynamic Sign Language Dataset (Video-Based)
5. Preprocessed static sign language datasets:
Resized images to uniform dimensions.
Normalized pixel values for consistent input.
6. Preprocessed dynamic sign language datasets:
Extracted frames from .mp4 and .mov videos.
Stored extracted frames as .jpg images for training.
(II) Model Development
7. Implemented CNN model for static sign recognition (A-Z, "del", "nothing", "space").
8. Implemented CNN-LSTM model for dynamic sign recognition (video-based).
9. Trained ResNet model for ASL & ISL image classification.
10. Trained MobileNetV2 model for lightweight classification.
11. Optimized data loading using .npy format for faster training.
12. Reduced training lag and GPU overload issues.
(III) Testing and Predictions
13. Image-based prediction:

User uploads an image, and the model predicts the sign.
14. Video-based prediction:

Extracts frames from video, processes them through CNN-LSTM, and predicts the sign.
Sequential image upload for word formation:

User uploads multiple images of letters, and the model combines them into a word.
(IV) Interactive Learning Mode
15. Step-by-step letter checking:

User uploads letter-by-letter to spell a word.
Model checks if each letter is correct.
16. Real-time testing and feedback:

User uploads an image, and the model gives immediate feedback.
Generated words from letter predictions.

(V) Model Improvement and Fine-Tuning
17. Fine-tuned models with additional data.
18. Updated models using transfer learning (ResNet and MobileNetV2) for higher accuracy.
19. Implemented model learning mode:
Model updates itself with newly learned data.
(VI) Deployment and Finalization
20. Saved updated models in .h5 format for future use.
21. Provided a testing script for easy evaluation and verification.
