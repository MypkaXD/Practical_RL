# DQN

Deep Q-Network - алгоритм RL, который объединяет Q-Learning и DeepLearning. Служит для работы с большими или непрерывными пространствами состояний.

Сеть на вход принимает состояние s и за один проход выдает предсказанное Q-value для любого действия из данного состояния s.

Loss function = $E[(r+\gamma * max_{a'}Q(s',a',\theta) - Q(s,a,\theta))^2]$ 

Для поиска точки минимума используется обычный GD (gradient descent): $W_{i+1}=W_{i}-{LearningRate}*\frac{dL}{dw}$ 

