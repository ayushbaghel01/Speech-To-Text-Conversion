# Speech Recognition with ESPnet Models

## Objective:
The objective of this code is to perform `automatic speech recognition` (ASR) using `pre-trained ESPnet` models. It involves transcribing speech audio files into text and evaluating the transcription accuracy using metrics such as Word Error Rate (`WER`) and Character Error Rate (`CER`).

## Approach:
1. **Installation**:
   - Install the required Python package containing pre-trained ESPnet models using the following command:
     ```
     ! pip install -q espnet_model_zoo
     ```

2. **Model Download**:
   - The code downloads and unpacks a specific ESPnet model. In this example, it uses the model tagged `'Shinji Watanabe/spgispeech_asr_train_asr_conformer6_n_fft512_hop_length256_raw_en_unnorm_bpe5000_valid.acc.ave'`.

3. **Speech Recognition**:
   - Speech recognition is performed on audio files located in a specified directory (`base_dir`). The code recursively traverses the directory structure to identify audio files.
   - The downloaded model is utilized to transcribe the speech into text. The recognized text is normalized using the `text_normalizer` function, which converts the text to lowercase and removes punctuation.

4. **Output Generation**:
   - The `recognized text` is written to an output file (`output_file_path`) for further analysis or integration into downstream applications.

5. **Evaluation**:
   - To assess the accuracy of the speech recognition, Word Error Rate (WER) and Character Error Rate (CER) are calculated using the TorchMetrics library.
   - The calculated WER and CER provide insights into the accuracy of the transcribed text compared to the ground truth.

## Requirements:
- Python 3.x
- `espnet_model_zoo` Python package
- PyTorch
- `TorchMetrics`
- SoundFile
- `Librosa`

   - ### To install the above dependencies, run the following command:
     ```
     ! pip install -r requirements.txt
     ```
## Usage:
1. **Setup**:
   - Ensure all required libraries are installed using the provided installation command.
   
2. **Configuration**:
   - Specify the directory containing audio files (`base_dir`) and the output file path (`output_file_path`) in the code.

3. **Execution**:
   - Run the code to perform speech recognition and evaluation.
   
4. **Analysis**:
   - Review the output file containing the recognized text for each audio file.
   - Assess the performance of the speech recognition system by analyzing the calculated WER and CER.
## Results:
- The `Word Error Rate` is: `0.264`
- The `Character Error Rate` is : `0.153`
