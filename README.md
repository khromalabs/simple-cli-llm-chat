**Simple CLI LLM Chat**
======================

Simple python script which provides a CLI to interact with a Large Language Model (LLM) using the LiteLLM library.

Started this script as an self-educational project but found it so useful that now it has turned into my AI daily-driver.

**Features**
------------

* Supports as much LLM providers as LiteLLM supports
* Configure your own servers as default servers
* Automatic chat backup to a file
* Interactive and non-interactive modes
* Code block extraction in non-interactive mode
* Customizable prompt style

**Usage**
---------

### Interactive Mode

1. Run the script without any arguments.
2. Type a message and press Enter to receive a response from the AI.
3. Press Ctrl+C to exit.

### Non-Interactive Mode

1. Pipe a message to the script using `echo "message" | python ai.py`.
2. The script will process the message and print the response.
3. Use the `-s` or `--strip` option to extract only code blocks from the response.
* `-h` or `--help`: Display usage information.
* `-l` or `--light`: Use a light theme for the prompt.
* `-s` or `--strip`: Extract only code blocks from the response in non-interactive mode.
* `-m` or `--model`: Specify a custom LLM model.

To see how you must define the model look in the [LiteLLM documentation](https://litellm.vercel.app/docs/providers), API keys must be defined using environment variables as defined there.

**Configuration**
---------------

* The script uses the `PROVIDERS` list to configure LLM providers. Add or modify providers as needed.
* The `BACKUP` variable specifies the file path for automatic chat backup.

**Requirements**
---------------

* Python 3.x
* LiteLLM library
* requests library
* prompt_toolkit library

**License**
-------

This script is released under the MIT License. See LICENSE.txt for details.
