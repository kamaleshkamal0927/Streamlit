import streamlit as st

st.title("Streamlit Online Input Demo")

name = st.text_input("Enter your name")
age = st.number_input("Enter your age", min_value=0, max_value=120)

if st.button("Submit"):
    st.success(f"Hello {name} 👋")
    st.write("Age:", age)
