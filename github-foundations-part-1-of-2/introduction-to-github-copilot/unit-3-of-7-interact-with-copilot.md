# Interact with Copilot

Copilot has features and capabilities that may not be obvious
Learning Copilot features can improve productivity

There are various ways to trigger Copilot and shortcuts you can use
Multiple Copilot features, shortcuts and triggers can help you code faster

## Inline suggestions

The most immediate form of Copilot assistance is inline suggestions
Copilot watches you code and autocompletes to make inline suggestions

To accept a Copilot suggestion, press `Tab` or `>`, to reject it press `Esc` or just keep typing
Copilot watches you code and offers suggestions ahead of you in greyed out text which you can accept or reject

Inline suggestions are especially useful when you are doing repetitive tasks or boilerplate
Copilot offers suggestions so you can autocomplete boilerplate or repetitive tasks

## Command palette

The Visual Studio Code command palette offers quick access to Copilot:
1. `Ctrl + Shift + P` (or `Cmd + Shift + P` for Mac)
2. Enter **Copilot**
3. Select required actions

Copilot provides suggestions inline, and actions from the command palette

## Copilot chat

1. Open Copilot Chat in your IDE
2. Prompt Copilot with natural language

Copilot offers suggestions, and can be accessed from the command palette or Copilot chat

Copilot can provide examples to help you explore unfamiliar coding concepts or syntax
Copilot offers inline suggestions and can respond to prompts with examples to help you learn

## Inline chat

For context-specific help, you can use inline chat
1. Place the cursor where you want assistance
2. `Ctrl + I` (or `Cmd + I` for Mac)
3. Give prompts specific to the cursor location

Copilot offers inline suggestions, and can be accessed with command palette, Copilot chat or even inline chat

With inline chat you can get targeted assistance for a specific section of code
Copilot gives inline suggestions, targeted assistance with inline chat, and general assistance with chat or command palette

Slash commands are used to call actions simply by typing them in the editor
Watch inline suggestions, target assistance with inline chat, do actions with command palette, do actions faster with slash commands, or get general assistance with chat

**Examples:**
- `/explain` explain the selected code
- `/suggest` suggest code for this context
- `/tests` generate unit tests for selected function or class
- `/comment` convert comment to code snippet

## Comments to code

Copilot can convert natural language comments to code when you press the `Enter` key for quick drafting
Copilot has inline suggestions, targeted assistance with inline chat, actions in command palette, faster actions with slash commands, comment to code, and general chat assist

**Example**
```
# Function to reverse a string
def reverse_string(s):
    # Copilot suggests the function body here
```
**Result**
```
## Function to reverse a string
def reverse_string(s):
    return s[::-1]
```
## Multiple suggestions

Copilot offers multiple suggestions for complex code snippets so you can select the most appropriate
1. Look for the 💡 icon next to a suggestion
2. When you see it, press `Alt + ]` (or `Option + ]` for Mac) to cycle through suggestions

Copilot can offer multiple inline suggestions, provide context-specific assistance, perform actions and offer general assistance in chat

## Explanations

Learn and review code quickly with explanations
1. Select code block
2. Right-click > select *Copilot: Explain This*
3. Read the explanation

Copilot not only offers general assistance, but can cycle through multiple suggestions, respond to slash commands for fast action and even explain specific blocks of code

## Automated test generation

Copilot can generate unit tests for you
1. Select a function or class
2. Use the command palette (Ctrl + Shift + P) > select *Copilot: Generate Unit Tests*
3. Review test cases

Copilot not only offers general assistance, but targeted context-specific assistance, fast actions with slash commands, multiple explanations and even generated unit tests

**Example**
```
def add(a, b):
    return a + b

# Copilot might generate a test like this:
def test_add():
    assert add(2, 3) == 5
    assert add(-1, 1) == 0
    assert add(0, 0) == 0
```

Copilot learns from context, so keeping your code well structured and commented will improve its responses over time
GitHub Copilot learns from context to provide multiple suggestions, perform actions, explain code and even generate unit tests
