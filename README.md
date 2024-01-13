# Password Checker

This Python script checks the strength of passwords by querying the "Have I Been Pwned" (HIBP) database. It also indicates if the password has been previously compromised and provides suggestions for updating it.

## How It Works

The script uses the [Pwned Passwords API](https://haveibeenpwned.com/API/v3#PwnedPasswords) to check if a password has been previously exposed in data breaches. It converts the password into a SHA-1 hash and queries the API with the first five characters of the hash. The API then returns a list of hash suffixes with associated breach counts. The script matches the hash suffix of the provided password and informs the user if it has been compromised.

## Usage

1. Make sure you have Python installed on your system.
2. Clone this repository or download the `passwordchecker.py` file.
3. Open a terminal or command prompt.
4. Navigate to the directory where `passwordchecker.py` is located.
5. Run the following command:

    ```bash
    python passwordchecker.py your_password1 your_password2 ...
    ```

   Note: If you are using Windows, you might need to use `python3` instead of `python` in the command.

6. The script will check the provided passwords and display whether they have been compromised.

## Example

```bash
python passwordchecker.py MyStrongPassword Password123
reponse // MyStrongPassword was not found. Carry on.
// Password123 was found 456789 times... you should change the password.
```

## Dependencies

This script uses the `requests` library for making HTTP requests. You can install it using:

```bash
pip install requests
```

Feel free to customize the script or integrate it into your projects. If you have any suggestions or improvements, please create an issue or submit a pull request.
