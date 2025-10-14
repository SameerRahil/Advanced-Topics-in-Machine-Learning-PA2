Modern vision systems are trained on one distribution and
then deployed on another, and even small changes in texture,
style, background, or class frequency can cause large out of
domain drops. This paper studies three practical responses
in one reproducible framework so that results are easy to
compare and extend. First, we look at unsupervised domain
adaptation (UDA) where the target has no labels; we bench-
mark classic alignment methods (DAN, DANN, CDAN)
against a strong and simple self-training baseline, and we do
not only report target accuracy but also per-class behavior on
rare categories, a proxy domain discriminability score (via
a small domain classifier on features), and t-SNE overlays
to visualize how alignment interacts with class separability.
Second, we consider domain generalization (DG) from mul-
tiple labeled sources to an unseen target and compare ERM,
IRM, Group DRO, and SAM while holding the backbone,
augmentations, learning-rate schedule, and seeds fixed for
fairness; we report average and worst-source accuracy in
addition to the target, and we probe the loss surface (and the
radius rho) with one-dimensional parameter perturbations to
connect flatter minima with better OOD performance. Third,
we explore prompt-based robustness with CLIP: we com-
pare zero-shot and linear-probe baselines to prompt learning
with a light unlabeled-target regularizer, and we instrument
gradient cosine similarity across domains on prompt or last-
layer parameters to detect when updates conflict so that
alignment methods like PGA become motivated and inter-
pretable.

We acknowledge the help and guidance of our great instructor, Sir Muhammad Tahir, faculty of Electrical Engineering in the EE Department of Lahore University of Management Sciences (LUMS), Lahore, Pakistan, and also the efforts of our TAs Abdullah Bin Faisal and Haseeb Tahir.
