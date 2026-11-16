# Perception for Autonomous Systems (34759)

Course material and my work for DTU 34759 *Perception for Autonomous Systems*:

| Folder pattern | Contents |
|---|---|
| `N exercise - …` | Weekly exercise notebooks and data |
| `N exercise solution - …` | Solutions to the weekly exercises |
| `N project - …` | Small projects (K-means, Kalman ball tracking, MNIST classifier, stereo visual odometry) |
| `PFAS lectures/` | Lecture slides (PDF) |
| `Sample Exam Material*/` | Sample exam data |

The code targets the conda environment `pfas` (Python 3.10, OpenCV, Open3D, NumPy, SciPy, scikit-learn, Matplotlib).

## Install the offline docs

The offline documentation (~2.5 GB) is too large for git. It's attached to this repo's
[`docs` release](https://github.com/madsclaussen/pfas/releases/tag/docs) as three archives.
Run this from the repo root:

```bash
cd pfas

# Download (with the GitHub CLI)
gh release download docs -R madsclaussen/pfas

# ...or without gh
for f in offline-docs opencv-5.0-docs open3d-0.20-docs; do
  curl -LO "https://github.com/madsclaussen/pfas/releases/download/docs/$f.tar.gz"
done

# Extract and clean up
for f in offline-docs.tar.gz opencv-5.0-docs.tar.gz open3d-0.20-docs.tar.gz; do
  tar -xzf "$f"
done
rm offline-docs.tar.gz opencv-5.0-docs.tar.gz open3d-0.20-docs.tar.gz

# Open the index
xdg-open "OFFLINE DOCS - START HERE.html"    # macOS: open, Windows: start
```

This creates `Offline docs/`, `OpenCV 5.0 docs/` and `Open3D 0.20 docs/`. They're already
in `.gitignore`. Everything works fully offline: MathJax, jQuery and Plotly are bundled locally.

### What's included

| Library | Version | Archive | Online version |
|---|---|---|---|
| NumPy | 2.2 | `offline-docs.tar.gz` | https://numpy.org/doc/2.2/ |
| SciPy | 1.15.3 | `offline-docs.tar.gz` | https://docs.scipy.org/doc/scipy-1.15.3/ |
| pandas | 2.3.3 | `offline-docs.tar.gz` | https://pandas.pydata.org/pandas-docs/version/2.3.3/ |
| scikit-learn | 1.7 | `offline-docs.tar.gz` | https://scikit-learn.org/1.7/ |
| scikit-image | 0.25 | `offline-docs.tar.gz` | https://scikit-image.org/docs/0.25.x/ |
| Matplotlib (PDF) | 3.10.9 | `offline-docs.tar.gz` | https://matplotlib.org/3.10.9/ |
| Python | 3.10 | `offline-docs.tar.gz` | https://docs.python.org/3.10/ |
| OpenCV | 5.0 | `opencv-5.0-docs.tar.gz` | https://docs.opencv.org/5.x/ |
| Open3D | 0.20 | `open3d-0.20-docs.tar.gz` | https://www.open3d.org/docs/0.20.0/ |
