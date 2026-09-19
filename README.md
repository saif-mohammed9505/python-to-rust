# Python to Rust Code Converter

An AI-powered tool that converts Python code into Rust code using Large Language Models (LLMs). The project supports multiple AI models and provides an interactive Gradio interface for Python-to-Rust code conversion.

## Technologies Used

- Python
- Rust
- OpenAI Python SDK
- OpenRouter
- Hugging Face
- Ollama
- DeepSeek
- Qwen
- Llama 3.2
- Gradio
- Jupyter Notebook

## Features

- Convert Python code into Rust using AI
- Support for multiple LLMs
- DeepSeek support through Hugging Face
- Qwen support through Hugging Face
- Llama 3.2 support through Ollama
- Run Python code
- Generate Rust code automatically
- Save generated Rust code as `main.rs`
- Interactive Gradio interface
- Large code generation support
- Compare Python and Rust implementations

## How It Works

```text
Python Code
     |
     v
Select AI Model
     |
     +---- DeepSeek
     |
     +---- Qwen
     |
     +---- Llama 3.2
     |
     v
AI Code Generation
     |
     v
Generated Rust Code
     |
     v
main.rs
```

The project sends the Python code to the selected AI model with instructions to generate high-performance Rust code that produces equivalent output.

## Requirements

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### requirements.txt

```text
openai
python-dotenv
huggingface-hub
ipython
gradio
```

## AI Models

### DeepSeek

The project uses:

```text
deepseek-ai/DeepSeek-V3-0324
```

through Hugging Face.

### Qwen

The project uses:

```text
Qwen/Qwen3.5-9B
```

through Hugging Face.

### Llama 3.2

The project can use:

```text
llama3.2
```

through Ollama.

Install the model using:

```bash
ollama pull llama3.2
```

## Environment Variables

Create a `.env` file in the project directory.

```env
OPENROUTER_API_KEY=your_openrouter_api_key
HUGGING_FACE_API=your_huggingface_api_key
```

Do not upload `.env` or API keys to GitHub.

## Project Structure

```text
python-to-rust/
│
├── python_to_rust.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

Generated files such as `main.rs` should not be committed if they are only temporary outputs.

## Gradio Interface

The project provides an interactive Gradio interface with:

- Python code input
- Rust code output
- AI model selection
- Convert button

The workflow is:

```text
Python Code
     |
     v
Select Model
     |
     v
Convert
     |
     v
Generated Rust Code
```

The available model options in the interface are:

- DeepSeek
- Qwen
- Llama 3.2

## Code Conversion

The AI model receives a system prompt instructing it to:

- Convert Python code into high-performance Rust
- Produce equivalent output
- Optimize the implementation where possible
- Return only Rust code

The generated response is cleaned and returned as Rust source code.

## Performance Example

## Example: Python to Rust Conversion

### Python Code

```python
def calculate_sum(numbers):
    total = 0

    for number in numbers:
        total += number

    return total


numbers = [10, 20, 30, 40, 50]

result = calculate_sum(numbers)

print("Sum:", result)
```

### Converted Rust Code

```rust
fn calculate_sum(numbers: &[i32]) -> i32 {
    let mut total = 0;

    for number in numbers {
        total += number;
    }

    total
}

fn main() {
    let numbers = vec![10, 20, 30, 40, 50];

    let result = calculate_sum(&numbers);

    println!("Sum: {}", result);
}
```

### Output

```text
Sum: 150
```

The Python code is provided as input to the selected AI model, which generates the equivalent Rust implementation. The generated Rust code can then be reviewed and, with the appropriate Rust toolchain, compiled and executed.

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/python-to-rust.git
cd python-to-rust
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure API Keys

Create a `.env` file:

```env
OPENROUTER_API_KEY=your_openrouter_api_key
HUGGING_FACE_API=your_huggingface_api_key
```

### 5. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
python_to_rust.ipynb
```

Run the notebook cells in order.

### 6. Launch the Gradio Interface

The notebook launches the Gradio interface locally.

A local URL similar to the following will be displayed:

```text
http://127.0.0.1:7868
```

Open the URL in your browser.

## Important Notes

- AI-generated Rust code should be tested before use.
- Generated code may not always be correct for every Python program.
- Python and Rust have different language features and runtime behavior.
- Complex Python programs may require additional Rust libraries or manual modifications.
- Execution time depends on the machine and generated implementation.
- The project is intended for educational and experimental purposes.

## Security

Never commit API keys or secrets to GitHub.

The following files should remain local:

```text
.env
.venv/
__pycache__/
.ipynb_checkpoints/
```

These files should be excluded using `.gitignore`.

## Future Improvements

- Improve Python-to-Rust conversion accuracy
- Add Rust compilation and execution
- Add automatic correctness testing
- Add automatic performance benchmarking
- Support more AI models
- Support more Python libraries
- Add downloadable Rust source files
- Improve error handling
- Add cross-platform Rust toolchain support

## 📌 Repository

GitHub Repository:

https://github.com/saif-mohammed9505/python-to-rust

---

## 👨‍💻 Author

**Saif Mohammed**

GitHub:

https://github.com/saif-mohammed9505

---

## License

This project is intended for educational and experimental purposes.
