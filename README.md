# PPTX to Kahoot Question Generator 🎉

<img src="https://github.com/SurgeonTalus/PPTX-to-AI-Kahoot-Questions-in-.xlsx-LM-studio-Qwen2.5/blob/main/PowerpointKahootLogo.png" alt="PowerPoint to Kahoot Logo" width="300" align="right">

## What is this?
This script extracts text from PowerPoint slides and uses an AI model to generate multiple-choice questions in markdown, witch is then converted to a.xlsx file that can be uloaded to Kahoot. 

Perfect for teachers, trainers, and anyone who wants to turn presentations into interactive quizzes with minimal effort! 🚀

## How Does It Work? 🤔
1. Select a PowerPoint (.pptx) file or an entire folder.
2. The script scans the slides, extracts text, and sends it to an AI model.
3. The AI returns multiple-choice questions in a table format.
4. The script saves the questions as an Excel file, ready to upload to Kahoot.

## How to Run 🏃‍♂️
### Prerequisites 📋
Make sure you have Python installed. Then, install the required dependencies:
```sh
pip install python-pptx requests openpyxl tkinter
```
### Running the Script 🏁
1. Open a terminal or command prompt.
2. Run the script:
   ```sh
   python "PowerPoint to Kahoot Generator.py"
   ```
3. A file dialog will appear. Choose a PowerPoint file or folder
4. The script processes the file(s) and saves a new Excel file with questions.
5. Alternatively, open the file in VS code, and just hit the run button. Ask copilot inside of VS code if it does not run.

## Uploading to Kahoot 📤
1. Go to [Kahoot](https://create.kahoot.it/)
2. Click **"Create new Kahoot"**
3. Click the **Add question** button on the left panel.
4. In the window that pops up, find the **Import spreadsheet** option in the bottom right corner.

![Uploading Excel to Kahoot](https://github.com/SurgeonTalus/PPTX-to-AI-Kahoot-Questions-in-.xlsx-LM-studio-Qwen2.5/blob/main/UpladExcelToKahoot.png)

## Example of Generated File 📂

![Generated Questions](https://github.com/SurgeonTalus/PPTX-to-AI-Kahoot-Questions-in-.xlsx-LM-studio-Qwen2.5/blob/main/QuetionsGenerated.png)

## Changing the AI Model 🤖
The script uses a local AI model. To change the model, update this section in `process_pptx_file`:
```python
"model": "qwen2.5-7b-instruct-1m",
```
Replace it with the desired model name.

## Modifying the AI Prompt 📝
The AI prompt is located in the `data` dictionary:
```python
{"role": "system", "content": "In markdown. Language Norwegian if detected. Make 5 Questions..."}
```
Change the text inside `"content"` to adjust the question format or language.
If you want to run a newer model, ask AI to help you google the formating for other models and then apply the adjusted code.

## Running the AI Model Locally ⚙️
1. Easy, Open LM studio. Download the suggested model. Press the turn on server button. Dubble check that port defaults to `1234`.
2. If needed, adjust the `url` in this function:
```python
url = "http://localhost:1234/v1/chat/completions"
```

## Need Help? 💡
If you get stuck, feel free to ask for help or suggest improvements. Let's make learning fun! 🎉

