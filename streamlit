import streamlit as st
import pandas as pd

# Page config
st.set_page_config(page_title="Simple Streamlit App", layout="centered")

# Title
st.title("📊 Simple Streamlit App")

# User input section
st.header("User Details")

name = st.text_input("Enter your name")
age = st.number_input("Enter your age", min_value=0, max_value=120)
city = st.selectbox("Select your city", ["Chennai", "Bangalore", "Hyderabad", "Mumbai"])

# Button action
if st.button("Submit"):
    if name.strip() == "":
        st.warning("Please enter your name")
    else:
        st.success(f"Welcome {name} 👋")
        st.write("Age:", age)
        st.write("City:", city)

st.divider()

# CSV Upload Section
st.header("Upload CSV File")

uploaded_file = st.file_uploader("Upload a CSV file", type=["csv"])

if uploaded_file is not None:
    df = pd.read_csv(uploaded_file)
    st.success("File uploaded successfully!")
    st.write("Preview of data:")
    st.dataframe(df.head())

    st.write("Dataset Info:")
    st.write("Rows:", df.shape[0])
    st.write("Columns:", df.shape[1])

st.divider()

# Footer
st.caption("Built with Streamlit 🚀")
