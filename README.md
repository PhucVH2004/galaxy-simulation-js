# 🌌 3D Galaxy Simulation (Mô phỏng Thiên Hà 3D)



> **English:** A high-performance, interactive 3D Galaxy Simulation built with Three.js. It combines accurate Keplerian orbital physics with custom GLSL shaders to create a vast, multi-layered universe.
>
> **Tiếng Việt:** Dự án mô phỏng Thiên hà 3D tương tác hiệu năng cao được xây dựng bằng Three.js. Kết hợp vật lý quỹ đạo Kepler chính xác với các shader GLSL tùy chỉnh để tạo ra một vũ trụ đa tầng lớp rộng lớn.

---

## 📸 Screenshots (Hình ảnh)

*(Place your screenshot here / Hãy thay thế dòng này bằng ảnh chụp màn hình dự án của bạn)*
`![Galaxy Screenshot](./screenshot.png)`

---

## ✨ Key Features (Tính năng nổi bật)

### 1. Hybrid Visual System (Hệ thống hình ảnh lai)
- **Shader Particles:** Uses custom GLSL Vertex & Fragment shaders for the galactic core, creating a glowing, dynamic nebula effect without heavy texture loads.
- **Physical Bodies:** Standard meshes (`SphereGeometry`) for stars and planets that interact with light.

### 2. Multi-Layered Universe (Vũ trụ Đa lớp)
The simulation is divided into 3 distinct depth layers:
- **Layer 1: Galactic Core (0 - 300u):** A dense, colorful cloud of gas and stars using additive blending.
- **Layer 2: Asteroid Belt (320u - 550u):** A massive ring of rocky asteroids surrounding the core.
- **Layer 3: Outer Space (600u - 1500u):** Sparse, faint celestial bodies representing the vastness of deep space.

### 3. Physics & Interaction (Vật lý & Tương tác)
- **Keplerian Orbits:** Objects move based on simplified orbital mechanics ($v \propto \sqrt{1/r}$), moving faster near the center and slower at the edges.
- **Smart Controls:** - `OrbitControls` with damping for smooth movement.
  - **Zoom Fix:** Prevents the camera from clipping into the black hole center (min distance constrained).
  - Parallax effect created by different rotation speeds of layers.

---

## 🛠 Tech Stack (Công nghệ sử dụng)

- **Core:** HTML5, CSS3, Modern JavaScript (ES6 Modules).
- **3D Engine:** [Three.js](https://threejs.org/).
- **Rendering:** WebGL.
- **Shaders:** GLSL (OpenGL Shading Language).

---

## 🚀 How to Run (Cách chạy dự án)

Since this project uses ES6 Modules (`import ... from ...`), it **cannot** be run by simply opening the `.html` file directly in the browser (due to CORS policy). You need a local server.

### Option 1: VS Code (Recommended)
1. Install the **Live Server** extension in Visual Studio Code.
2. Right-click on `index.html`.
3. Select **"Open with Live Server"**.

### Option 2: Python
If you have Python installed, open your terminal in the project folder and run:
```bash
# Python 3
python -m http.server 8000
