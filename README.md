 # GPT Review Text

 This script allows you to review selected text using ChatGPT and preserve the original writing style.
 It fetches the selected text from the clipboard, sends it to the OpenAI API, and pastes the reviewed text back into the active application.

 ## Dependencies
 - xsel
 - curl
 - jq
 - xdotool

 ## Installation (Ubuntu and derivatives)

 ```bash
 sudo apt update
 sudo apt install xsel curl jq xdotool
 ```

 ## Obtaining an OpenAI API Key
 1. Go to https://platform.openai.com/ and log in or create an account.
 2. Navigate to **API Keys** in the dashboard.
 3. Click **Create new secret key** and copy the generated key.
 4. Create a `.env` file in the project root with:

    ```bash
    API_KEY=your_openai_api_key_here
    MODEL=gpt-4.1-nano
    ```

 ## Configuration
 Ensure the `.env` file is in the same directory as the `review-text` script.
 The script reads the `API_KEY` and `MODEL` environment variables at runtime.

 ## Usage
 1. Select the text you want to review in any application.
 2. Run the script:

    ```bash
    ./review-text
    ```

 3. The reviewed text will be pasted automatically.

 ## Custom Shortcut (Ubuntu GNOME)
 To set a custom keyboard shortcut (e.g., Win + R):

 1. Open **Settings** > **Keyboard Shortcuts**.
 2. Scroll to **Custom Shortcuts** and click **+**.
 3. Enter:
    - **Name:** Review Text
    - **Command:** /full/path/to/review-text
 4. Click on **Set Shortcut**, press **Super + R** (Win + R), and confirm.
 5. Make sure the new shortcut is enabled.

 Now, when you press **Super + R**, the script will run on the selected text.

## How to Use

In any application (e.g., your web browser), write or open the text you want to improve. Then:

1. Select the text you wish to review.
2. Press **Super+R** (Win + R) or your configured shortcut.
3. The script will send the selected text to ChatGPT and automatically paste the improved version in place.

## Author

Developed by **Fábio Berbert de Paula**. For inquiries, please contact via [LinkedIn](https://www.linkedin.com/in/fabio-linux/) or email at [fberbert@gmail.com](mailto:fberbert@gmail.com).

## License

This project is licensed under the MIT License. See https://opensource.org/licenses/MIT for details.
