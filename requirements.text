# Import required libraries
import streamlit as st
import numpy as np
import time

# Configure page settings
st.set_page_config(
    page_title="AI Career Predictor Pro",
    page_icon="🤖",
    layout="centered"
)

# Custom colourful gradient theme
st.markdown("""
<style>
.stApp {
    background: linear-gradient(135deg, #667eea, #764ba2);
    color: white;
}
h1, h2, h3 {
    text-align: center;
}
.block-container {
    padding-top: 2rem;
}
</style>
""", unsafe_allow_html=True)

# Website Title
st.title("🤖 AI Career Predictor Pro")
st.write("### Mathematics Behind AI – Function Fusion Model")
st.write("---")

# Input Section
st.subheader("📊 Enter Your Marks")

math = st.slider("Maths", 0, 100, 60)
science = st.slider("Science", 0, 100, 60)
english = st.slider("English", 0, 100, 60)
biology = st.slider("Biology", 0, 100, 60)

st.write("---")

st.subheader("💡 Rate Your Interest (1-10)")

interest_tech = st.slider("Technology Interest", 1, 10, 5)
interest_creative = st.slider("Creative Interest", 1, 10, 5)
interest_medical = st.slider("Medical Interest", 1, 10, 5)

st.write("---")

# Prediction Button
if st.button("🚀 Run AI Prediction"):

    # Loading animation
    with st.spinner("AI is analyzing using Function Fusion Model..."):
        time.sleep(2)

    # AI Mathematical Model (Weighted Linear Functions)
    engineering_score = (0.40*math + 0.35*science + 0.25*interest_tech*10)
    medical_score = (0.45*biology + 0.35*science + 0.20*interest_medical*10)
    arts_score = (0.40*english + 0.30*interest_creative*10 + 0.30*science)

    # Store scores
    scores = {
        "Engineering": engineering_score,
        "Medical": medical_score,
        "Arts & Humanities": arts_score
    }

    # Decision Function (argmax)
    career = max(scores, key=scores.get)

    # Confidence Calculation
    total_score = sum(scores.values())
    confidence = (scores[career] / total_score) * 100

    # Display Results
    st.success(f"🎯 AI Predicted Career: {career}")
    st.info(f"🤖 Confidence Level: {round(confidence, 2)} %")

    # Display Chart
    st.bar_chart(scores)

    st.write("---")

    # AI Explanation Section
    st.subheader("🧠 How This AI Works")

    st.write("""
    🔹 Linear Combination:
    f(x) = w₁x₁ + w₂x₂ + w₃x₃

    🔹 Function Fusion:
    Multiple weighted functions combined.

    🔹 Scaling Function:
    Interest × 10 adjusts preference weight.

    🔹 Decision Rule:
    Career selected using argmax (maximum score).

    🔹 Confidence Formula:
    Confidence = (Highest Score / Total Score) × 100

    This demonstrates how Mathematics builds the foundation of Artificial Intelligence systems.
    """)