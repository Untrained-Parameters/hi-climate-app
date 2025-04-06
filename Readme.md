# 🌴 Hawaiʻi Climate Explorer

A visual, interactive web app for exploring climate data across the Hawaiian Islands, built with [Streamlit](https://streamlit.io/). The app displays daily and monthly temperature and rainfall data from the Hawaiʻi Climate Data Portal (HCDP) using maps, charts, and forecasts. It is designed for educators, researchers, students, and residents interested in climate patterns and trends across the state.

---

## 🚀 Demo: How to Run the App

### 🔧 Requirements

- Python 3.11+
- Docker and Docker Compose installed on your system.

### ▶️ Launch the app locally

#### Using Docker Compose
1. Clone the repository and the submodules:
   ```bash
   git clone https://github.com/your-repo/hi-climate-app.git --recursive
   cd hi-climate-app
   ```

2. Start the services using Docker Compose:
   ```bash
   docker compose up --build
   ```

3. Access the app in your browser at `http://localhost`.

#### Without Docker
1. Install dependencies:
   ```bash
   pip install -r weather-data-analysis-dashboard/requirements.txt
   ```

2. Run the frontend:
   ```bash
   cd weather-data-analysis-dashboard
   streamlit run app/main.py
   ```

3. Run the backend:
   ```bash
   cd ../hi-climate-backend
   uvicorn app.main:app --reload --port 8000
   ```

4. Access the app in your browser at `http://localhost:8501`.

---

## 📂 Project Structure

- **`weather-data-analysis-dashboard`** — Frontend built with Streamlit for interactive visualizations and user interface.
- **`hi-climate-backend`** — Backend built with FastAPI to handle API requests and integrate with Google GenAI tools for chat functionality.
- **`docker-compose.yml`** — Defines the services for the frontend, backend, and a Caddy reverse proxy.
- **`caddy`** — Configuration for the Caddy reverse proxy to route requests between the frontend and backend.

---

## 🛠️ Technologies Used

- **Frontend**: [Streamlit](https://streamlit.io/) for building interactive dashboards and visualizations.
- **Backend**: [FastAPI](https://fastapi.tiangolo.com/) for handling API requests and integrating with external services.
- **Chat Integration**: [Google GenAI](https://cloud.google.com/genai) tools for providing conversational AI capabilities.
- **Containerization**: Docker and Docker Compose for easy deployment and service orchestration.
- **Reverse Proxy**: Caddy for routing requests between services.

---

## 🧠 Features

- 🌡️ **Daily & Monthly Data** for each island.
- 📍 **Interactive Map Views** (rainfall & temperature).
- 📊 **Island Comparison Bar Charts**.
- ⏩ **Rainfall Forecasting** using a local machine learning model.
- 📅 **Time Filtering** via sidebar controls.
- 💬 **Custom Chat UI** powered by Google GenAI for climate-related Q&A.

---

## 📡 Data Source

All climate data are pulled in real time from the [Hawaiʻi Climate Data Portal API](https://www.hcdp.hawaii.edu/), provided by the University of Hawaiʻi.

---

## 🐳 Docker Compose Services

- **Frontend**: Runs the Streamlit app on port `8501`.
- **Backend**: Runs the FastAPI server on port `8000`.
- **Caddy**: Reverse proxy for routing requests between the frontend and backend.

---

## 🤝 Acknowledgments

This app was developed as part of the **2025 AI Hackathon** at the University of Hawaiʻi at Mānoa, by a multidisciplinary team of students, including Federica Chiti (Astronomy), Dhvanil Desai (Astronomy), Fahim Yasir (Electrical & Computer Engineering), Gerardo Rivera Tello (Atmospheric Sciences), and Yada Ponpittayalert (Design).

---

## 📬 Contact

For questions or contributions, feel free to open an issue or reach out via [GitHub Discussions](https://github.com/your-repo/discussions).
```