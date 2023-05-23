# Speculative Sampling
Simple and minimal implementation of [Accelerating Large Language Model Decoding with Speculative Sampling](https://arxiv.org/pdf/2302.01318.pdf) in NumPy for GPT-2. See [`main.py`](https://github.com/jaymody/speculative-sampling/blob/main/main.py). I also wrote a [blog post](https://jaykmody.com/blog/speculative-sampling/) for this implementation.

**Install Dependencies**:
```bash
pip install -r picoGPT/requirements.txt
```
Tested on `Python 3.9.10`.

**Usage**:
```python
python main.py --prompt "The United States invaded Russia and" -n_tokens_to_generate 20  --draft_model_size "124M" --target_model_size "1558M" --K 4 --models_dir '/Volumes/Crucial X6/Develop/models'
```

Which outputs:
```text
Autoregressive Decode
---------------------
Time = 71.64s
Text = Alan Turing theorized that computers would one day become so powerful that they would be able to think like humans.

In the 1950s, he proposed a way to build a computer that could think like a human. He called it the "T

Speculative Decode
------------------
Time = 30.11s
Text = Alan Turing theorized that computers would one day become so powerful that they would be able to think for themselves. But it's not just computers that are capable of thinking for themselves.

In fact, the brain is a computer, and it's capable
```
