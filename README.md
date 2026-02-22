# Market-Specific-Language-Signals

In this project, we worked with a public SMS corpus (NUS SMS Corpus). One can *think of it as anonymized customer messages* from a messaging product.

Each line of the dataset is a JSON object representing one message, including:
- `text`: the message text
- `country`: the user's country (we will use **"Singapore"** and **"United States"** only)
- `userID`: the user's ID
- other fields (not needed for this assignment)

There are two files:
- `sms_small.jsonl` (small dataset, for quick debugging)
- `sms.jsonl` (full dataset, for the final run)

# Task 1

The goal is to output **24 lines**: the 12 most *distinctive* tokens for **Singapore** and the 12 most *distinctive* tokens for **United States**.

# Task 2

In real messaging products, raw token counts are often dominated by a few power users. A token might look “distinctive” simply because one user sends it many times. For example, user #123 always say "sorry" in the messages he/she sends to others. In this task, instead of finding globally distinctive tokens between Singapore and the United States, you will now identify market-distinctive tokens that are consistent across users.

The goal is still to output **24 lines**: the 12 most *distinctive* tokens for **Singapore** and the 12 most *distinctive* tokens for **United States**, but only for tokens whose distinctiveness is **NOT** driven by a small number of heavy users.
