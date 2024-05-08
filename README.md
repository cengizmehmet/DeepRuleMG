# Hybrid Intelligent Control System for Adaptive Microgrid Optimization: Integration of Rule-Based Control and Deep Learning Techniques

Microgrids (MGs) have evolved as critical components of modern energy distribution networks, providing increased dependability, efficiency, and sustainability. Effective control strategies are essential for optimizing MG operation and maintaining stability in the face of changing environmental and load conditions. Traditional rule-based control systems are extensively used due to their interpretability and simplicity. However, these strategies frequently lack the flexibility for complex and changing system dynamics. This paper provides a novel method called hybrid intelligent control for adaptive MG that integrates basic rule-based control and deep learning techniques, including gated recurrent units (GRUs), basic recurrent neural networks (RNNs), and long short-term memory (LSTM). The main target of this hybrid approach is to improve MG management performance by combining the strengths of basic rule-based systems and deep learning techniques. These deep learning techniques readily enhance and adapt control decisions based on historical data and domain-specific rules, leading to increasing system efficiency, stability, and resilience in adaptive MG. Our results show that the proposed method optimizes MG operation, especially under demanding conditions such as variable renewable energy supply and unanticipated load fluctuations. This study investigates special RNN architectures and hyperparameter optimization techniques with the aim of predicting power consumption and generation within the adaptive MG system. Our promising results show the highest-performing models indicating high accuracy and efficiency in power prediction. The finest-performing model accomplishes an R2 value close to 1, representing a strong correlation between predicted and actual power values. Specifically, the best model achieved an R2 value of 0.999809, an MSE of 0.000002, and an MAE of 0.000831.

## Cite Us

This work was first published in MDPI Energies ([https://www.mdpi.com/1996-1073/17/10/2260](https://www.mdpi.com/1996-1073/17/10/2260)). If you use our data or models scripts, please cite the following [bibkey](CITE.md):

      @Article{en17102260,
        AUTHOR = {Akbulut, Osman and Cavus, Muhammed and Cengiz, Mehmet and Allahham, Adib and Giaouris, Damian and Forshaw, Matthew},
        TITLE = {Hybrid Intelligent Control System for Adaptive Microgrid Optimization: Integration of Rule-Based Control and Deep Learning Techniques},
        JOURNAL = {Energies},
        VOLUME = {17},
        YEAR = {2024},
        NUMBER = {10},
        ARTICLE-NUMBER = {2260},
        URL = {https://www.mdpi.com/1996-1073/17/10/2260},
        ISSN = {1996-1073},
        DOI = {10.3390/en17102260}
      }

## Results

\begin{table}[H]

 \captionsetup{width=1.0\linewidth,justification=raggedright}
    \caption{The %MDPI: We remove verticle lines, please check (CONFIRMED).
 results of the best RNN-based architectures---order of $R^2$.}
    \label{tab:best}
\begin{adjustwidth}{-\extralength}{0cm}
   
  \newcolumntype{C}{>{\centering\arraybackslash}X}
		\begin{tabularx}{\fulllength}{LLLLLLL}
 
    \hline
        \textbf{Optimizer} & \textbf{LR\_Sch} & \textbf{Batch Size} & \textbf{Arch\_Details} & \textbf{Test\_R2} & \textbf{Test\_MSE} & \textbf{Test\_MAE}  \\ \hline
        adam & constant & 7 & GRU(50) & 0.999809 & 0.000002 & 0.000831  \\ \hline
        adam & constant & 7 & GRU(15) & 0.999780 & 0.000003 & 0.001037  \\ \hline
        adam & constant & 7 & LSTM(50) & 0.999731 & 0.000003 & 0.000798  \\ \hline
        adam & constant & 7 & sRNN(50) & 0.999468 & 0.000006 & 0.001499  \\ \hline
        rmsprop & constant & 7 & GRU(50) & 0.999466 & 0.000055 & 0.001366  \\ \hline
        rmsprop & constant & 7 & sRNN(50) & 0.999457 & 0.000005 & 0.001246  \\ \hline
        rmsprop & constant & 7 & GRU(15) & 0.999223 & 0.000012 & 0.001820  \\ \hline
        adam & constant & 7 & LSTM(15) & 0.999041 & 0.000010 & 0.001433  \\ \hline
        rmsprop & constant & 7 & GRU(15) + GRU(15) & 0.998331 & 0.000022 & 0.002302  \\ \hline
        rmsprop & constant & 7 & LSTM(10) & 0.997685 & 0.000026 & 0.002008  \\ \hline
        rmsprop & constant & 7 & GRU(50) + GRU(50) + GRU(50) & 0.997464 & 0.000034 & 0.003154  \\ \hline
        rmsprop & constant & 7 & LSTM(50) + LSTM(50) + LSTM(50) & 0.993648 & 0.000071 & 0.002782  \\ \hline
        adam & constant & 7 & LSTM(15) + LSTM(15) + LSTM(15) & 0.989356 & 0.000117 & 0.002773  \\ \hline
        rmsprop & constant & 7 & LSTM(15) + LSTM(15) + LSTM(15) & 0.983175 & 0.000175 & 0.004793  \\ \hline
        adam & constant & 7 & LSTM(10) + LSTM(10) & 0.982457 & 0.000190 & 0.002483  \\ \hline
        rmsprop & constant & 7 & LSTM(5) + LSTM(5) & 0.975035 & 0.000278 & 0.005464  \\ \hline
        sgd & constant & 7 & LSTM(10) & 0.833051 & 0.001675 & 0.019741  \\ \hline
        sgd & constant & 7 & LSTM(5) & 0.824882 & 0.001812 & 0.017543  \\ \hline
        adam & constant & 7 & sRNN(5) & 0.797054 & 0.002377 & 0.017024  \\ \hline
        rmsprop & constant & 7 & GRU(5) & 0.780668 & 0.002561 & 0.007525  \\ \hline
    \end{tabularx}
\end{adjustwidth}
\end{table}
