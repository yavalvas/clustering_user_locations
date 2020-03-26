The final map with clusters is stored in GCloud, open link to render:
[https://storage.cloud.google.com/clustering_demo/clustering_result.html](
https://storage.cloud.google.com/clustering_demo/clustering_result.html)

To open jupyter notebook code:

1. Install Anaconda distribution with Jupyter Lab
2. Launch
```bash
jupyter lab
```
3. Create 'data' folder and copy there files with data

Initially it was started in colab, though interactive maps couldn't be embedded to it.
Notebooks use Google API from GCloud project to visualize and localize points on map.

- [Notebook with the source code](clustering_time_series_positions.ipynb)
Jupyter Lab was used for it. Other packages versions are specified in this file at the end with pip list.
It works with conda environment, additional dependencies installed inside the notebook without extra requirements.txt file.

- [Notebook saved to html](clustering_time_series_positions_notebook.html)
For the case if there aren't dependencies.
Some of the maps weren't preserved in it, so they are saved to the separate html files described below

- [Resampled coordinates](resampled_coordinates.html)
All coordinates undersampled, every 3rd is taken and visualized on GMaps.

- [Pure heatmap](pure_heatmap.html)
Heatmap plotted by the API, some clusters are visible.

- [Initial clustering attempt](initial_clustering_attempt.html)
First attempt of clustering without taking into consideration speed of the user.

- [Clustering result][clustering_result.html]
Clustering with a trick searching for the local minima points for the speed.
Points have different color depending on the support.
Closest locations appear on hover and on click on the points, as well the support number for the cluster.
Some locations with top support are listed in the notebook.
