java c
AMATH 481/581 Autumn Quarter 2024
Homework 3: Quantum Harmonic Oscillator
DUE: Friday, November 1 at midnight
(a) Rerun your homework 2 results to produce the eigenfunctions (A1) and eigenvalues (A2)
ANSWERS: Should be written out as A1 (eigenfunctions) and A2 (eigenvalues)
(b) Calculate the first five normalized eigenfunctions (ϕn) and eigenvalues (εn) using a direct method. Be sure to use a forward- and backward-differencing for the boundary conditions (HINT: 3 + 2∆x√KL2 − εn ≈ 3).
For this calculation, use x ∈ [−L, L] with L = 4 and choose xspan = −L : 0.1 : L. Save the absolute value of the eigenfunctions in a 5-column matrix (column 1 is ϕ1, column 2 is ϕ2 etc.) and the eigenvalues in a 1x5 vector. NOTE: This procedure solves for the interior points. So be sure at the end to include your first and last point.
ANSWERS: Should be written out as A3 (eigenfunctions) and A4 (eigenvalues)
(c) There has been suggestions that in some cases, nonlinearity plays a role such that
dx2/d 2ϕn − [γ|ϕn|2 + Kx2 − εn] ϕn = 0 .                                 (1)
Depending upon the sign of γ, the probability density is focused or defocused. Find the first two normalized modes for γ = ±0.05 using shooting. For this calculation, use x ∈ [−L, L] with L = 2 and choose xspan = −L : 0.1 : L. Save the absolute value of the eigenfunctions in a 2-column matrix (column 1 is ϕ1 and column 2 is ϕ2) and the eigenvalues in a 1x2 vector.
ANSWERS: For γ = 0.05, should be written out as A5 (eigenfunctions) and A6 (eigenvalues)
ANSWERS: For γ = −0.05, should be written out as A7 (eigenfunctions) and A8 (eigenvalues)
(d) For a fixed value of the energy (specifically, take εn = 1, γ = 0 with x ∈ [−L, L] and L = 2. For initial launch conditions, take ϕ = 1 and ϕx =√KL2 − 1), do a convergence study by controlling the error tolerance
ptions = {’rtol’: TOL, ’atol’: TOL}
solve_ivp(hw1_rh代 写AMATH 481/581 Autumn Quarter 2024 Homework 3: Quantum Harmonic OscillatorPython
代做程序编程语言s_a, x_span, y0, method=’RK45’, args=(E,), **options)
Show that indeed the schemes are fourth order (RK45) and second order (RK23) respectively by running the computation across the computational domain and adjusting the tolerance. Use specifically the following values of T L = [1e − 4 1e − 5 1e − 6 1e − 7 1e − 8 1e − 9 1e − 10]. In particular, plot on a log-log scale the average step-size (x-axis) using the diff and mean command versus the tolerance (y-axis) for the above tolerance values. What are the slopes of these lines? Use the POLYFIT command to get the slopes. Note that the local error should be O(∆t5) and O(∆t3) respectively. What are the local errors for Radau and BDF? Save the slopes computed from the POLYFIT command with the log-log of the data as a 4x1 vector with the slopes of RK45, RK23, Radau and BDF respectively.
ANSWERS: Should be written out as A9
(e) Compare your solutions in both (a) and (b) of homework 1 with the exact Gauss-Hermite polynomial solutions for this problem (See wikipedia.com, for instance). Compute the error between your numerical solution and the exact solution for the values of the eigenfunctions and eigenvalues computed above. Specifically, calculate the following quantity for each eigenfunction ∥ |ϕnumericaln| − |ϕexactn| ∥ where ∥f(x)∥ =R −LLf(x)2dx.
For the eigenvalues, simply calculate the relative percent error 100 × (|εnumericaln − εexactn|/εexactn). The error vectors associated with the eigenfunctions and eigenvalues should be 5x1 vectors.
ANSWERS: For part (a), should be written out as A10 (eigenfunctions) and A11 (eigenvalues)
ANSWERS: For part (b), should be written out as A12 (eigenfunctions) and A13 (eigenvalues)
NOTE: For the tolerances in both the convergence (shooting method) of the εn in (a) and (c), and in the area for part (c), use a tolerance of 10−4.







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
