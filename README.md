# 🔮 Playing Tetris with DQN

> Thanks to [Yiyuan](https://codemyroad.wordpress.com/2013/04/14/tetris-ai-the-near-perfect-player/) and [Artem](https://towardsdatascience.com/self-learning-ai-agents-part-ii-deep-q-learning-b5ac60c3f47) for their amazing articles that help me started this repo. Also [Spinning Up](https://spinningup.openai.com/en/latest/) developed by OpenAI is a great tool for beginners to get their hands dirty with RL. 

## Navigate Through the Files

<ul>
    <li>**agent.py**: define the class `DQNAgent`</li>
    <li>**tetris.py**: create the environment `Tetris`</li>
    <li>**run.py**: train the model and store weights in `ckpts/`  </li>
    <li>logs.py: log historical data (e.g. avg_score) in `logs/` </li>
    <li>eval.py: load weights and evaluate </li>
</ul>

## Attributes Used as Game State

<ul>
    <li>Number of lines cleared</li>
    <li>Number of holes</li>
    <li>Bumpiness</li>
    <li>Total height </li>
</ul>

## How to Use

### Install Dependencies

```
pip install -r requirements.txt
```

### Train the Model

```
python run.py
```

By default the environment is rendered every 50 episodes. Set `render = False` if you don't want any rendering.

### View the Logging Info

```
tensorboard --logdir=<your-logs-directory>
```

Substitute `<your-logs-directory>` with the path of your `logs` folder.

Enter the localhost link prompted in your browser to access TensorBoard.

### Load Weights & Evaluate

Replace line 28 of  `eval.py` with `<your-highest-score-ckpt-directory>`.

Run the `eval.py` to see the smartest agent you trained playing tetris! 

Feel free to twist the hyperparameters and train the agent with a further say, 2000 episodes.