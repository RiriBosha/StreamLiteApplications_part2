import streamlit as st

# Bonus: Sidebar for Language Switching
lang = st.sidebar.radio("🌐 Select Language / اختر اللغة", ["English", "العربية"])

if lang == "English":
    st.title("📊 Student Grade Calculator")
    st.markdown("### Calculate your overall academic performance")
    st.info("Enter your scores (0 to 100) for all four subjects below.")

    # 5 Widgets: slider, number_input, selectbox, radio, checkbox
    math = st.number_input("Math Score", 0.0, 100.0, 85.0)
    science = st.number_input("Science Score", 0.0, 100.0, 90.0)
    english = st.number_input("English Score", 0.0, 100.0, 78.0)
    history = st.number_input("History Score", 0.0, 100.0, 88.0)
    
    scale = st.radio("Grading Scale", ["Standard (A >= 90)", "Strict (A >= 95)"])
    confirm = st.checkbox("I confirm all scores are correct.")

    if st.button("Calculate Grade"):
        if not confirm:
            st.warning("Please check the confirmation box first.")
        else:
            avg = (math + science + english + history) / 4
            st.markdown(f"**Average Score:** `{avg:.2f} / 100`")

            a_cutoff = 95.0 if "Strict" in scale else 90.0
            b_cutoff = 85.0 if "Strict" in scale else 80.0

            if avg >= a_cutoff:
                st.success(f"🎉 Excellent! Grade: **A** ({avg:.1f}%)")
            elif avg >= b_cutoff:
                st.info(f"👍 Good Job! Grade: **B** ({avg:.1f}%)")
            elif avg >= 70.0:
                st.warning(f"⚠️ Passing Grade: **C** ({avg:.1f}%)")
            else:
                st.error(f"❌ Needs Improvement: Grade: **F** ({avg:.1f}%)")

else:
    st.title("📊 حاسبة الدرجات الدراسية")
    st.markdown("### احسب أداءك الأكاديمي العام")
    st.info("أدخل درجاتك (من 0 إلى 100) للمواد الأربع أدناه.")

    math = st.number_input("درجة الرياضيات", 0.0, 100.0, 85.0)
    science = st.number_input("درجة العلوم", 0.0, 100.0, 90.0)
    english = st.number_input("درجة اللغة الإنجليزية", 0.0, 100.0, 78.0)
    history = st.number_input("درجة التاريخ", 0.0, 100.0, 88.0)
    
    scale = st.radio("نظام التقدير", ["قياسي (ممتاز >= 90)", "صارم (ممتاز >= 95)"])
    confirm = st.checkbox("أؤكد أن جميع الدرجات صحيحة.")

    if st.button("حساب التقدير"):
        if not confirm:
            st.warning("يرجى تحديد مربع التأكيد أولاً.")
        else:
            avg = (math + science + english + history) / 4
            st.markdown(f"**المعدل العام:** `{avg:.2f} / 100`")

            a_cutoff = 95.0 if "صارم" in scale else 90.0
            b_cutoff = 85.0 if "صارم" in scale else 80.0

            if avg >= a_cutoff:
                st.success(f"🎉 ممتاز! التقدير: **أ (A)** ({avg:.1f}%)")
            elif avg >= b_cutoff:
                st.info(f"👍 جيد جداً! التقدير: **ب (B)** ({avg:.1f}%)")
            elif avg >= 70.0:
                st.warning(f"⚠️ مقبولة! التقدير: **ج (C)** ({avg:.1f}%)")
            else:
                st.error(f"❌ يحتاج تحسين! التقدير: **راسب (F)** ({avg:.1f}%)")
