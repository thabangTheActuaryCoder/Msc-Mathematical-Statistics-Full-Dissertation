# Figures Directory

Place all figures (images, diagrams, plots) for this chapter here.

Supported formats:
- `.pdf` - Best for vector graphics
- `.png` - Good for screenshots and raster images
- `.jpg` - Compressed image format
- `.eps` - Encapsulated PostScript

Reference figures in the corresponding `.tex` file using:
```latex
\includegraphics[width=0.8\textwidth]{Chapter X/Figures/figure_name.pdf}
```

For figures with captions:
```latex
\begin{figure}[h]
  \centering
  \includegraphics[width=0.8\textwidth]{Chapter X/Figures/figure_name.pdf}
  \caption{Figure caption here}
  \label{fig:figure_label}
\end{figure}
```
