# Far-field-diffraction-pattern
Propagating the field from a single slit experiment using the Scipy and animating the result with matplotlib.
Analytically well-understood case of a single-slit experiment. The sequence of Fourier transforms performed on the aperture field distribution was implemented in Python to resolve the far-field diffraction pattern–––given in one-dimension below up to a normalization constant of $2\pi$. I used the $|scipy fft|$ package which contains the Fast Fourier Transform (FFT) algorithm to perform,
\begin{equation}
\begin{aligned}
   E(x,z) = \mathcal{F}^{-1}\{E(k_x) e^{-i k_z z}\}
\end{aligned}
\label{eqn:Diffraction}
\end{equation}

where $E(k_x) = \mathcal{F}\{E(x,z_{0})\}$ and $k_z$ is given by the dispersion relation, $k_x^2 + k_y^2 + k_z^2 = \left( \frac{\omega}{c}\right)^2$; in one dimension,  $k_z = \sqrt{\left( \frac{\omega}{c}\right)^2 - k_x^2}$.

In FRED, a commercial Ray-tracing software, I simulated a 60$\mu$m x 1.3mm single slit illuminated by rays with a wavelength of 0.63$\mu$m. I resolved both the narrow and long dimensions using the propagation routine from eq. ~\eqref{eqn:Diffraction} at a distance of 50mm from the slit.
