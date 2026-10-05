# Ramp and Projectile Lab Simulation

An interactive, high-precision HTML5/JavaScript physics simulation for kinematics, dynamics, and projectile motion.  
It models the motion of a solid steel sphere rolling down an incline, crossing a laboratory table (with adjustable surface friction $\mu$), passing through an optical photogate sensor, and launching as a projectile onto the floor.

Try it live 🔗 https://atreyuartax.github.io/Ramp-Projectile-Simulator/

---

## 🔬 Lab Modes

### Lab 1: Predict Projectile Range
Students configure the ramp height, incline angle, table height, and surface friction, then calculate the predicted landing range ($R$) before testing their predictions in the simulator.

### Lab 2: Determine Acceleration Due to Gravity ($g$)
The app measures and displays the ball's instantaneous launch velocity ($v_x$) via an optical **Photogate Sensor** (or video inspection) at the table edge.  
Students record:
- Vertical drop ($\Delta d_y$)
- Horizontal launch velocity ($v_x$)
- Horizontal landing distance ($\Delta d_x$)
- Flight time ($t$)

Using kinematic principles (with initial vertical velocity $v_{iy} = 0$):
$$t = \frac{\Delta d_x}{v_x}, \quad \Delta d_y = \frac{1}{2} g t^2 \implies g_{\text{exp}} = \frac{2 \Delta d_y}{t^2} = \frac{2 \Delta d_y v_x^2}{(\Delta d_x)^2}$$

Students compare their experimental $g_{\text{exp}}$ against the accepted standard ($9.81\text{ m/s}^2$) and calculate their percent error:
$$\text{Percent Error} = \frac{|g_{\text{exp}} - 9.81|}{9.81} \times 100\%$$

An interactive **Calculation Checker** and **Trial Log Table** allow students to verify their math and record data across multiple heights.

---

## ✨ Features

- **High-Precision Physics**:
  - Exact analytical impact calculation (eliminates discrete Euler frame overshoot).
  - Solid sphere rotational dynamics ($a = \frac{5}{7} g \sin\theta$).
  - Device-independent metric geometry calibrated for consistent results on any screen size.
  - Safe friction handling that brings the ball to rest cleanly without reverse acceleration.
- **Simulation Modes**:
  - **Math Mode (Ideal)**: Zero measurement error ($g_{\text{exp}} = 9.8100\text{ m/s}^2$ exact).
  - **Real Mode (Experimental)**: Incorporates realistic laboratory measurement uncertainty ($\pm 2.5\%$).
- **Modernized Visuals & High-DPI Rendering**:
  - Crisp Retina / 4K canvas rendering with device pixel ratio (DPR) scaling.
  - Detailed laboratory composite table with metric ruler markings and plumb line.
  - Active photogate with infrared beam and animated LED indicator.
  - Smooth trajectory trail, dynamic altitude shadow, and floor landing dimension markers.
  - Light / Dark theme toggle.
- **Playback Controls**:
  - Play, Pause/Resume, Single-Frame Step, and Reset.
  - Multi-speed playback ($0.25\times$, $0.5\times$, $1.0\times$).

---

## 🚀 Usage

1. Open `index.html` (or `table_ramp.html`) in any modern web browser.
2. Select **Lab 1: Predict Range** or **Lab 2: Determine Gravity ($g$)**.
3. Adjust the parameters using the sliders or numeric input fields.
4. Click **Start Simulation**.
5. In Lab 2, use the measured values to calculate $g$, check your answer, and record trials in the data table.

No build tools or external servers required—runs 100% locally in the browser.

---

## 📄 License

This project is licensed under the MIT License.
