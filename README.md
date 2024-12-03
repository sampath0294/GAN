import streamlit as st

st.title("Generative Art with GAN")
if st.button("Generate Art"):
    noise = np.random.normal(0, 1, (1, 100))
    art = generator.predict(noise)[0]
    st.image((art * 255).astype(np.uint8), use_column_width=True)
