# Aryabhata 1.0 Evaluations

This repository contains comprehensive evaluations of Arayabhata 1.0 model on JEE 2025 Mathematics questions, and comparisons with models like GPT-4o-mini and Qwen-2.5-math.

**Original Aryabhata 1.0 Project**: [Aryabhata 1.0 on Hugging Face](https://huggingface.co/PhysicsWallahAI/Aryabhata-1.0)

## Project Overview

The project evaluates the mathematical reasoning capabilities of Aryabhata 1.0 by testing them on authentic JEE (Joint Entrance Examination) January 2025 Mathematics questions. The evaluation includes:

- **Question Processing**: Extracting and formatting JEE 2025 mathematics questions
- **Model Response Generation**: Generating responses from LMs
- **Answer Evaluation**: Comparing model responses with correct answers
- **Performance Analysis**: Comprehensive scoring and analysis of model performance

## Project Structure

```
Aryabhata1.0Evals/
├── Evals/                          # Evaluation results for different models
│   ├── aryabhata1.0/              # Aryabhata 1.0 model evaluations
│   ├── gpt-4o-mini/               # GPT-4o-mini model evaluations
│   └── qwen-2.5-math/             # Qwen-2.5-math model evaluations
├── Notebooks/                      # Jupyter notebooks for analysis and processing
├── question_papers/                # Source JEE 2025 mathematics questions
├── Documentation/                  # Analysis reports and documentation
│   ├── Report.md                  # Comprehensive evaluation report
│   ├── ClaimVsReality.md          # Claims vs reality analysis
│   ├── recommendations.md         # Key recommendations and improvements
│   └── quickref.md                # Quick reference summary
└── readme.md                       # This file
```

## Detailed Folder Structure

### 📁 `question_papers/`
Contains the source JEE January 2025 Mathematics questions organized by date and shift.

**Files:**
- `master_jee2025_maths_questions.json` - Master file containing all JEE 2025 mathematics questions
- `jan_22_shift_1_questions.json` - January 22, 2025, Shift 1 questions
- `jan_22_shift_2_questions.json` - January 22, 2025, Shift 2 questions
- `jan_23_shift_1_questions.json` - January 23, 2025, Shift 1 questions
- `jan_23_shift_2_questions.json` - January 23, 2025, Shift 2 questions
- `jan_24_shift_1_questions.json` - January 24, 2025, Shift 1 questions
- `jan_24_shift_2_questions.json` - January 24, 2025, Shift 2 questions
- `jan_28_shift_1_questions.json` - January 28, 2025, Shift 1 questions
- `jan_28_shift_2_questions.json` - January 28, 2025, Shift 2 questions
- `jan_29_shift_1_questions.json` - January 29, 2025, Shift 1 questions
- `jan_29_shift_2_questions.json` - January 29, 2025, Shift 2 questions
- `question_papers.json` - Consolidated question papers

**Question Format:**
Each question contains:
- `question`: The mathematical problem text
- `options`: Multiple choice options (A, B, C, D)
- `answer`: The correct answer

### 📁 `Evals/`
Contains evaluation results for different LLM models.

#### `aryabhata1.0/`
Evaluation results for the Aryabhata 1.0 model.

**Files:**
- `final_score_card.csv` - Final performance metrics for all question sets
- `overall_score_card.csv` - Overall performance summary
- `only_question_YYYYMMDD_HHMMSS/` - Timestamped evaluation folders containing:
  - `pred_only_question_YYYYMMDD_HHMMSS_[date]_shift_[1/2]_questions.json` - Model predictions and responses

**Response Format:**
Each response contains:
- Original question and options
- `aryabhata_response_Wquestion`: Full model response with system prompts
- `aryabhata_response_Wquestion_cleaned`: Cleaned response text
- `extract_ans_from_boxed`: Extracted answers from boxed format
- `check_ex_answer`: Expected correct answer
- `converted_answers`: Processed model answer
- `Matched`: Boolean indicating if answer matches expected
- Token counts and inference time metrics

#### `gpt-4o-mini/`
Evaluation results for GPT-4o-mini model.

**Files:**
- `final_score_card.csv` - Performance metrics
- `overall_score_card.csv` - Overall summary
- `gpt_responses/` - Model response files

#### `qwen-2.5-math 2/`
Evaluation results for Qwen-2.5-math model.

**Files:**
- `final_score_card.csv` - Performance metrics
- `overall_score_card.csv` - Overall summary
- `only_question_YYYYMMDD_HHMMSS/` - Timestamped evaluation folders

### 📁 `Notebooks/`
Jupyter notebooks for data processing, analysis, and evaluation.

**Files:**
- `Aryabhata1.0Evaluations.ipynb` - Main evaluation notebook for Aryabhata 1.0
- `Evaluations_qwen_2_5_math.ipynb` - Evaluation notebook for Qwen-2.5-math
- `Gen_responses_arayabhata1_0.ipynb` - Response generation for Aryabhata 1.0
- `GPT_4o_mini_Evals.ipynb` - Evaluation notebook for GPT-4o-mini
- `Parallael_answer_gen_qwen_2_5_math.ipynb` - Parallel response generation for Qwen-2.5-math

### 📁 `Documentation/`
Comprehensive analysis reports and documentation files.

**Files:**
- `Report.md` - **Comprehensive evaluation report** with detailed findings, performance analysis, and three-way model comparison
- `ClaimVsReality.md` - **Claims vs reality analysis** comparing Aryabhata 1.0 team's claims with actual performance
- `recommendations.md` - **Key recommendations** for improvements and future development
- `quickref.md` - **Quick reference summary** with visual comparisons and key findings

#### Key Documentation Overview:

**📊 Report.md**
- Detailed performance analysis of all three models
- Individual question set results with visual charts
- Quality issues analysis with concrete examples
- Three-way model comparison on same question sets
- Critical analysis and improvement recommendations

**⚖️ ClaimVsReality.md**
- Critical analysis of claimed vs actual performance
- 46% accuracy discrepancy identification
- Transparency and methodology concerns
- Recommendations for the Aryabhata team

**🎯 recommendations.md**
- Prioritized action items for immediate, short-term, and long-term improvements
- Technical recommendations for model development
- Standards recommendations for the research community
- Priority matrix with clear timelines

**📋 quickref.md**
- Executive summary of all findings
- Visual performance comparisons using ASCII charts
- Quick reference tables and rankings
- Links to all detailed documentation

## Evaluation Metrics

The evaluation system tracks various performance metrics:

### Score Card Metrics
- **Total Questions**: Number of questions in each set
- **Evaluated**: Number of questions successfully evaluated
- **Correct**: Number of correct answers
- **Incorrect**: Number of incorrect answers
- **Not Evaluated**: Questions that couldn't be evaluated
- **% Evaluated**: Percentage of questions successfully evaluated
- **Correct %**: Percentage of correct answers
- **Incorrect %**: Percentage of incorrect answers

### Token Usage Metrics
- **Input Tokens**: Number of tokens in input questions
- **Output Tokens**: Number of tokens in model responses
- **Prompt Tokens**: Number of tokens in system prompts
- **Total Tokens**: Total token usage

### Performance Metrics
- **Inference Time**: Time taken for model inference
- **LLM Judged**: Number of questions judged by LLM evaluators
- **Answer Matching**: Boolean indicators for correct answer matching

## Model Performance Summary

Based on the evaluation results:

### Aryabhata 1.0 Model
- **Overall Performance**: 40% accuracy on 250 questions (significantly below claimed 86%)
- **Best Performance**: 71.43% accuracy on Jan 22 Shift 1
- **Worst Performance**: 10% accuracy on Jan 24 Shift 1
- **Strengths**: Best mathematical accuracy among evaluated models
- **Critical Issues**: Severe repetition, hallucination, and response quality problems

### Three-Way Model Comparison
- **Aryabhata 1.0**: Best accuracy (58.14%) but has quality issues
- **GPT-4o-mini**: Best response quality and evaluation success (100%) but moderate accuracy (32%)
- **Qwen-2.5-math**: Poorest performance across all metrics (16.67% accuracy)

### Key Findings
- **46% accuracy gap** between claimed (86%) and actual (40%) performance
- **Severe quality issues** not reflected in original claims
- **Inconsistent performance** across different question sets
- **Token inefficiency** (2,423 avg tokens vs claimed ~2K)

### Documentation
For detailed analysis, see:
- **[Quick Reference](quickref.md)** - Executive summary with visual comparisons
- **[Comprehensive Report](Report.md)** - Detailed findings and analysis
- **[Claims vs Reality](ClaimVsReality.md)** - Critical analysis of performance claims
- **[Recommendations](recommendations.md)** - Actionable improvement suggestions

## Usage

### Running Evaluations
1. Navigate to the `Notebooks/` directory
2. Open the relevant evaluation notebook
3. Follow the setup instructions for API keys and dependencies
4. Run the evaluation cells to generate results

### Analyzing Results
1. Check the `Evals/` directory for specific model results
2. Review `final_score_card.csv` files for performance metrics
3. Examine individual response files for detailed analysis
4. Use notebooks for custom analysis and visualization

### Dependencies
- Python 3.8+
- Jupyter Notebooks
- Required packages (see notebook imports):
  - `langchain_google_genai`
  - `pandas`
  - `numpy`
  - `tqdm`
  - `json`

## Key Features

1. **Comprehensive Evaluation**: Multi-model comparison on authentic JEE questions
2. **Detailed Metrics**: Extensive performance tracking and analysis
3. **Structured Data**: Well-organized question and response formats
4. **Reproducible Results**: Timestamped evaluation runs
5. **Token Analysis**: Detailed token usage and cost analysis
6. **Answer Extraction**: Automated answer extraction and matching

## Contributing

To contribute to this evaluation framework:
1. Add new question sets to `question_papers/`
2. Implement new evaluation metrics in notebooks
3. Add support for additional LLM models
4. Improve answer extraction and matching algorithms

## License

This project is for educational and research purposes. Please ensure compliance with relevant terms of service for the LLM APIs used.

---

*This repository provides a comprehensive framework for evaluating mathematical reasoning capabilities of Arayabhata 1.0 using authentic JEE 2025 Mathematics questions.*
