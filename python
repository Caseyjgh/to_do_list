# app.py

import streamlit as st

# Initialize session state for the to-do list
if "todo_list" not in st.session_state:
    st.session_state.todo_list = []

st.title("📝 To-Do List App")

# Input to add a new item
new_item = st.text_input("Add a new to-do item:")
if st.button("Add"):
    if new_item:
        st.session_state.todo_list.append(new_item)
        st.success(f'Added: "{new_item}"')
    else:
        st.warning("Please enter a to-do item.")

# Display the current to-do list
if st.session_state.todo_list:
    st.subheader("Your To-Do List:")
    for i, item in enumerate(st.session_state.todo_list, 1):
        st.write(f"{i}. {item}")
else:
    st.info("Your to-do list is empty.")
