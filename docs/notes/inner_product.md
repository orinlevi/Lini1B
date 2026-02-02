# מכפלה פנימית

!!! info "שייך ללינארית 2ב"
    נושא זה נלמד בקורס **אלגברה לינארית 2ב** ולא בלינארית 1ב.

## הגדרה

<div class="definition-box" markdown>

**הגדרה:** מכפלה פנימית על מרחב וקטורי \( V \) מעל \( \mathbb{R} \) היא פונקציה:
\[ \langle \cdot, \cdot \rangle : V \times V \to \mathbb{R} \]

המקיימת:

1. **לינאריות בארגומנט הראשון:**
   - \( \langle u + v, w \rangle = \langle u, w \rangle + \langle v, w \rangle \)
   - \( \langle \alpha u, v \rangle = \alpha \langle u, v \rangle \)

2. **סימטריה:** \( \langle u, v \rangle = \langle v, u \rangle \)

3. **חיוביות:** \( \langle v, v \rangle \geq 0 \), ושוויון אם"ם \( v = 0 \)

</div>

---

## דוגמאות

<div class="example-box" markdown>

**המכפלה הסטנדרטית ב-\( \mathbb{R}^n \):**
\[ \langle u, v \rangle = u \cdot v = \sum_{i=1}^{n} u_i v_i \]

**מכפלה פנימית על \( C[a,b] \):**
\[ \langle f, g \rangle = \int_a^b f(x)g(x) \, dx \]

**מכפלה פנימית על \( M_n(\mathbb{R}) \):**
\[ \langle A, B \rangle = \text{tr}(A^T B) \]

</div>

---

## נורמה

<div class="definition-box" markdown>

**נורמה מושרית:** הנורמה המושרית ממכפלה פנימית:
\[ \|v\| = \sqrt{\langle v, v \rangle} \]

</div>

<div class="theorem-box" markdown>

**תכונות הנורמה:**
1. \( \|v\| \geq 0 \), ושוויון אם"ם \( v = 0 \)
2. \( \|\alpha v\| = |\alpha| \|v\| \)
3. **אי-שוויון המשולש:** \( \|u + v\| \leq \|u\| + \|v\| \)

</div>

---

## אי-שוויון קושי-שוורץ

<div class="formula-box" markdown>

**אי-שוויון קושי-שוורץ:**
\[ |\langle u, v \rangle| \leq \|u\| \cdot \|v\| \]

שוויון מתקיים אם"ם \( u, v \) תלויים לינארית.

</div>

---

## אורתוגונליות

<div class="definition-box" markdown>

**הגדרה:** שני וקטורים \( u, v \) **אורתוגונליים** (מסומן \( u \perp v \)) אם:
\[ \langle u, v \rangle = 0 \]

</div>

<div class="definition-box" markdown>

**קבוצה אורתוגונלית:** קבוצת וקטורים \( \{v_1, \ldots, v_n\} \) היא אורתוגונלית אם:
\[ \langle v_i, v_j \rangle = 0 \quad \forall i \neq j \]

**קבוצה אורתונורמלית:** קבוצה אורתוגונלית שבה \( \|v_i\| = 1 \) לכל \( i \).

</div>

---

## משלים אורתוגונלי

<div class="definition-box" markdown>

**משלים אורתוגונלי:** אם \( W \subseteq V \) תת-מרחב, אז:
\[ W^\perp = \{ v \in V : \langle v, w \rangle = 0 \; \forall w \in W \} \]

</div>

<div class="theorem-box" markdown>

**משפט:** \( V = W \oplus W^\perp \) (סכום ישר)

**מסקנה:** \( \dim(W) + \dim(W^\perp) = \dim(V) \)

</div>

---

## תהליך גרם-שמידט

<div class="theorem-box" markdown>

**משפט גרם-שמידט:** לכל קבוצה בלתי תלויה לינארית ניתן להפוך לקבוצה אורתונורמלית הפורשת את אותו תת-מרחב.

</div>

<div class="example-box" markdown>

**האלגוריתם:** נתונה קבוצה \( \{v_1, \ldots, v_n\} \) בלתי תלויה.

**שלב 1 - אורתוגונליזציה:**
\[ u_1 = v_1 \]
\[ u_k = v_k - \sum_{j=1}^{k-1} \frac{\langle v_k, u_j \rangle}{\langle u_j, u_j \rangle} u_j \]

**שלב 2 - נרמול:**
\[ e_k = \frac{u_k}{\|u_k\|} \]

</div>

---

## הטלה אורתוגונלית

<div class="definition-box" markdown>

**הטלה על תת-מרחב:** אם \( W \) תת-מרחב עם בסיס אורתונורמלי \( \{e_1, \ldots, e_k\} \), אז ההטלה של \( v \) על \( W \):
\[ \text{proj}_W(v) = \sum_{i=1}^{k} \langle v, e_i \rangle e_i \]

</div>

<div class="formula-box" markdown>

**הטלה על וקטור:**
\[ \text{proj}_u(v) = \frac{\langle v, u \rangle}{\langle u, u \rangle} u \]

</div>
