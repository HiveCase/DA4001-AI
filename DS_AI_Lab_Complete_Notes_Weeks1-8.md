<h1 align="center" style="color:#0d1b4c; background:linear-gradient(90deg,#a8edea,#fed6e3); padding:22px; border-radius:14px; font-family:Georgia,serif;">📘 Data Science &amp; AI Lab — Complete Revision Notes</h1>

<p align="center" style="font-size:16px; color:#333;">
<b>Weeks 1 → 8</b> &nbsp;|&nbsp; Detailed Notes · Full Syntax · Past-Exam Questions · Worked Solutions<br>
<i>Built from the official course site (Weeks 1–7), Week-8 slides, the Email-Assistant notebook, and the last two term papers.</i>
</p>

<div style="background:#fff8e1; border-left:6px solid #ffb300; padding:12px 16px; border-radius:6px;">
<b>How to use this guide</b><br>
Each week has three blocks:
<ol>
<li><b style="color:#1565c0;">📖 NOTES</b> — every definition, formula and function syntax you need.</li>
<li><b style="color:#6a1b9a;">❓ QUESTIONS</b> — the actual past-paper questions for that week, tagged with a <b>frequency/importance</b> badge. Duplicates are kept on purpose.</li>
<li><b style="color:#2e7d32;">✅ SOLUTIONS</b> — question + options + the correct answer with reasoning.</li>
</ol>
</div>

<div style="background:#e3f2fd; border-left:6px solid #1565c0; padding:12px 16px; border-radius:6px; margin-top:10px;">
<b>🔑 Importance badges</b> — how often the idea appears across the two papers:<br>
<span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span>
<span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span>
<span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span>
<span style="background:#546e7a;color:#fff;padding:2px 8px;border-radius:10px;">• STANDARD</span>
</div>

---

<h2 style="color:#0d1b4c;">🗺️ Master Index &amp; Topic → Week Map</h2>

<table style="border-collapse:collapse; width:100%;">
<tr style="background:#0d1b4c; color:#fff;">
<th style="padding:8px;">Week</th><th style="padding:8px;">Theme</th><th style="padding:8px;">Core Tools</th><th style="padding:8px;"># Past-Qs</th>
</tr>
<tr style="background:#f4f6ff;"><td style="padding:8px;">1</td><td style="padding:8px;">Python DS Stack Refresher</td><td style="padding:8px;">NumPy, Pandas, Matplotlib, Seaborn</td><td style="padding:8px;">5</td></tr>
<tr><td style="padding:8px;">2</td><td style="padding:8px;">Classical ML</td><td style="padding:8px;">Scikit-learn</td><td style="padding:8px;">5</td></tr>
<tr style="background:#f4f6ff;"><td style="padding:8px;">3</td><td style="padding:8px;">Deep Learning</td><td style="padding:8px;">PyTorch, TensorFlow</td><td style="padding:8px;">7</td></tr>
<tr><td style="padding:8px;">4</td><td style="padding:8px;">Computer Vision</td><td style="padding:8px;">OpenCV, PIL, CNNs, YOLO</td><td style="padding:8px;">7</td></tr>
<tr style="background:#f4f6ff;"><td style="padding:8px;">5</td><td style="padding:8px;">NLP &amp; LLMs</td><td style="padding:8px;">HuggingFace, Transformers, LoRA</td><td style="padding:8px;">6</td></tr>
<tr><td style="padding:8px;">6</td><td style="padding:8px;">Prompting &amp; LangChain</td><td style="padding:8px;">LangChain, LCEL, LLM APIs</td><td style="padding:8px;">6</td></tr>
<tr style="background:#f4f6ff;"><td style="padding:8px;">7</td><td style="padding:8px;">RAG &amp; Vector DBs</td><td style="padding:8px;">FAISS, Chroma, embeddings</td><td style="padding:8px;">6</td></tr>
<tr><td style="padding:8px;">8</td><td style="padding:8px;">Agents &amp; Autonomous AI</td><td style="padding:8px;">LangGraph, LangChain agents</td><td style="padding:8px;">8</td></tr>
</table>

---
<h1 id="week1" style="color:#fff; background:#1565c0; padding:16px; border-radius:12px;">🟦 WEEK 1 — Data Science &amp; Python Stack Refresher</h1>

<p style="color:#555;"><b>Tools:</b> NumPy · Pandas · Matplotlib · Seaborn · Jupyter · Git</p>

<h2 style="color:#1565c0;">📖 NOTES</h2>

<h3 style="color:#0d47a1;">1. NumPy — the numerical core</h3>

NumPy provides the <code>ndarray</code>: a fixed-type, N-dimensional array that is contiguous in memory, which makes vectorised math fast.

<b>Key attributes of an array <code>a</code>:</b>
<table style="border-collapse:collapse;">
<tr style="background:#e3f2fd;"><th style="padding:6px;border:1px solid #90caf9;">Attribute</th><th style="padding:6px;border:1px solid #90caf9;">Meaning</th></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;"><code>a.shape</code></td><td style="padding:6px;border:1px solid #90caf9;">tuple of dimension sizes, e.g. <code>(2, 5)</code></td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;"><code>a.ndim</code></td><td style="padding:6px;border:1px solid #90caf9;">number of dimensions (axes)</td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;"><code>a.size</code></td><td style="padding:6px;border:1px solid #90caf9;">total number of elements</td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;"><code>a.dtype</code></td><td style="padding:6px;border:1px solid #90caf9;">element data type, e.g. <code>int64</code></td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;"><code>a.T</code></td><td style="padding:6px;border:1px solid #90caf9;">transpose</td></tr>
</table>

<b>Array creation syntax</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import numpy as np

np.array([1, 2, 3])                 # from a Python list
np.zeros((2, 3))                    # 2x3 of 0.0
np.ones((2, 3))                     # 2x3 of 1.0
np.full((2, 2), 7)                  # filled with 7
np.eye(3)                           # 3x3 identity
np.arange(start, stop, step)        # like range(), stop EXCLUSIVE
np.linspace(start, stop, num)       # num evenly spaced points, stop INCLUSIVE
np.random.rand(2, 3)                # uniform [0,1)
np.random.randn(2, 3)              # standard normal
</pre>

<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Exam trap — <code>arange</code> vs <code>linspace</code>:</b> <code>np.arange(1, 11)</code> gives <code>[1,2,...,10]</code> (stop 11 excluded → 10 numbers). <code>reshape(2, 5)</code> then folds them row-major into 2 rows × 5 cols.
</div>

<b>Reshaping &amp; axis</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
a.reshape(2, 5)      # new shape, same data (row-major / C order)
a.reshape(-1, 1)     # -1 means "infer this dimension"
a.ravel()            # flatten to 1D
</pre>

<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧭 The single most-tested NumPy idea — <code>axis</code>:</b><br>
For a 2D array, <b>axis=0 collapses rows → column-wise result</b> (you move <i>down</i> each column).<br>
<b>axis=1 collapses columns → row-wise result</b> (you move <i>across</i> each row).<br>
Mnemonic: <i>"axis is the dimension that disappears."</i>
</div>

<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
X = np.arange(1, 11).reshape(2, 5)
# [[ 1  2  3  4  5]
#  [ 6  7  8  9 10]]
X.sum(axis=0)   # down columns -> [ 7  9 11 13 15]  (length = #cols = 5)
X.sum(axis=1)   # across rows   -> [15 40]            (length = #rows = 2)
X.sum()         # everything    -> 55
</pre>

Other reductions share the pattern: <code>.mean()</code>, <code>.max()</code>, <code>.min()</code>, <code>.std()</code>, <code>.argmax()</code>, <code>.cumsum()</code>.

<b>Vector / matrix products</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
x @ y            # matrix multiplication operator (PEP 465)
np.dot(x, y)     # same as @
np.matmul(x, y)  # same for 2D
x * y            # ELEMENT-WISE (Hadamard), NOT a dot product
np.outer(x, y)   # outer product -> 2D matrix
</pre>

<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ <code>@</code> on two 1-D arrays of equal shape → a scalar dot product</b> (∑ xᵢyᵢ). It is <b>not</b> element-wise and does <b>not</b> raise a SyntaxError.
</div>

<h3 style="color:#0d47a1;">2. Pandas — tabular data</h3>

Core objects: <code>Series</code> (1-D labelled) and <code>DataFrame</code> (2-D labelled table).

<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import pandas as pd
df = pd.DataFrame({'a':[1,2], 'b':[3,4]})
df.head(n)      df.tail(n)       # first / last n rows
df.info()       df.describe()    # schema / summary stats
df.shape        df.columns       df.dtypes
df['a']                          # a column (Series)
df.loc[row_label, col_label]     # label-based indexing
df.iloc[row_pos,  col_pos]       # position-based indexing
</pre>

<b>Combining tables — <code>pd.merge</code> (SQL-style joins)</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
pd.merge(left, right, on='key', how='inner')
#   how = 'inner' -> keep only keys present in BOTH   (intersection)
#         'left'  -> keep ALL left rows              (+ matches)
#         'right' -> keep ALL right rows
#         'outer' -> keep keys from EITHER            (union)
#         'cross' -> Cartesian product of every row pair
</pre>

<table style="border-collapse:collapse;">
<tr style="background:#e3f2fd;"><th style="padding:6px;border:1px solid #90caf9;">how</th><th style="padding:6px;border:1px solid #90caf9;">Rows kept</th><th style="padding:6px;border:1px solid #90caf9;">Use when…</th></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;">inner</td><td style="padding:6px;border:1px solid #90caf9;">keys in both</td><td style="padding:6px;border:1px solid #90caf9;">you want <b>only matching</b> rows</td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;">left</td><td style="padding:6px;border:1px solid #90caf9;">all of left</td><td style="padding:6px;border:1px solid #90caf9;">keep every left record</td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;">right</td><td style="padding:6px;border:1px solid #90caf9;">all of right</td><td style="padding:6px;border:1px solid #90caf9;">keep every right record</td></tr>
<tr><td style="padding:6px;border:1px solid #90caf9;">outer</td><td style="padding:6px;border:1px solid #90caf9;">union</td><td style="padding:6px;border:1px solid #90caf9;">keep everything, NaN-fill gaps</td></tr>
</table>

<b>Reshaping: pivot / melt / groupby</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
# LONG -> WIDE: turn distinct values of a column into new columns
df.pivot(index='Date', columns='City', values='Temp')
# pivot_table additionally aggregates duplicates:
df.pivot_table(index=..., columns=..., values=..., aggfunc='mean')

# WIDE -> LONG:
df.melt(id_vars=['Date'], value_vars=['NY','LA'])

# split-apply-combine:
df.groupby('City')['Temp'].mean()
df.groupby(['Date','City']).sum()   # aggregates, does NOT reshape to wide

df.transpose()   # swaps the whole axis; NOT the same as pivot
</pre>

<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ pivot vs transpose vs groupby:</b> To make each category its own column with another column as index, use <code>pivot(index=, columns=, values=)</code>. <code>transpose()</code> flips rows↔columns blindly; <code>groupby().sum()</code> aggregates but keeps long form.
</div>

<b>Element-wise transforms — apply &amp; map</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
s.map(func)                 # Series -> element-wise
df['c'].apply(func)         # Series -> element-wise
df.apply(func, axis=0/1)    # DataFrame -> per column (0) or per row (1)
df.applymap(func)           # DataFrame -> every cell (deprecated -> df.map)
</pre>

<h3 style="color:#0d47a1;">3. Matplotlib &amp; Seaborn — plotting</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import matplotlib.pyplot as plt
plt.plot(x, y)          # line
plt.scatter(x, y)       # scatter
plt.bar(x, heights)     # bar chart
plt.hist(data, bins=n)  # histogram
plt.xlabel(); plt.ylabel(); plt.title(); plt.legend()
plt.show()

import seaborn as sns   # high-level, works on DataFrames
sns.histplot(data=df, x='col')
sns.scatterplot(data=df, x='a', y='b', hue='label')
sns.heatmap(corr_matrix, annot=True)
sns.boxplot(data=df, x='cat', y='val')
</pre>

<h3 style="color:#0d47a1;">4. Git — quick reference</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
git init              git clone <url>
git status            git add <file>        git commit -m "msg"
git push              git pull
git branch <name>     git checkout <name>   git merge <name>
</pre>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 1</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span> <i>(pd.merge appears every term)</i><br>
You have <code>df_employees</code> and <code>df_departments</code>. You want the result to contain only employees who belong to a department that exists in the Departments table. Which <code>how=</code> should you use in <code>pd.merge()</code>?
<pre style="background:#f5f5f5;padding:8px;">result = pd.merge(df_employees, df_departments, on='dept_id', how=____)</pre>
A. <code>how='outer'</code> &nbsp; B. <code>how='left'</code> &nbsp; C. <code>how='inner'</code> &nbsp; D. <code>how='cross'</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
A "long" DataFrame has columns Date, City, Temp. You want each City as its own column with Date as index. Which command gives this wide-format table?<br>
A. <code>df.columns.tolist()</code><br>
B. <code>df.pivot(index='Date', columns='City', values='Temp')</code><br>
C. <code>df.groupby(['Date','City']).sum()</code><br>
D. <code>df.transpose()</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span> <i>(axis reductions repeat across both papers)</i><br>
Output of:
<pre style="background:#f5f5f5;padding:8px;">X = np.arange(1, 11).reshape(2, 5)
print(X.sum(axis=0))</pre>
A. <code>[5 7 9 11 13]</code> &nbsp; B. <code>[10 35]</code> &nbsp; C. <code>[45]</code> &nbsp; D. <code>[7 9 11 13 15]</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span> <i>(duplicate of the axis theme — kept intentionally)</i><br>
Output of:
<pre style="background:#f5f5f5;padding:8px;">A = np.array([[1,5,9],[10,2,1],[0,2,3]])
print(A.sum(axis=1))</pre>
A. <code>[15, 13, 5]</code> &nbsp; B. <code>[11, 9, 13]</code> &nbsp; C. <code>33</code> &nbsp; D. <code>[9, 10, 3]</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
<code>x</code> and <code>y</code> are 1D NumPy arrays with <code>x.ndim==1</code>, <code>y.ndim==1</code>, and <code>x.shape==y.shape</code>. What happens if you run <code>x @ y</code>?<br>
A. Dot product of the two vectors &nbsp; B. Outer product &nbsp; C. Element-wise product &nbsp; D. SyntaxError
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 1</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → C. <code>how='inner'</code></b><br>
"Only employees whose department exists in Departments" = keep rows whose <code>dept_id</code> is present in <b>both</b> tables = intersection = inner join. In the given data <code>emp_id 3</code> has <code>dept_id 99</code> (absent from Departments) → dropped by inner. <code>left</code> would keep Charlie with NaNs; <code>outer</code> adds the unmatched dept 30; <code>cross</code> ignores the key entirely.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → B. <code>df.pivot(index='Date', columns='City', values='Temp')</code></b><br>
<code>pivot</code> is the canonical long→wide reshape: index becomes rows, the distinct <code>City</code> values become columns, <code>Temp</code> fills the cells. <code>groupby().sum()</code> stays long; <code>transpose()</code> just flips axes; <code>columns.tolist()</code> only returns column names.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → D. <code>[7 9 11 13 15]</code></b><br>
Array is <code>[[1,2,3,4,5],[6,7,8,9,10]]</code>. <code>axis=0</code> collapses the rows (sums down each column): 1+6=7, 2+7=9, 3+8=11, 4+9=13, 5+10=15 → length 5. (Option B <code>[10 35]</code> would be <code>axis=1</code>.)
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → A. <code>[15, 13, 5]</code></b><br>
<code>axis=1</code> sums across each row: row0 1+5+9=15, row1 10+2+1=13, row2 0+2+3=5.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → A. Dot product</b><br>
For two 1-D arrays of equal length, <code>@</code> computes ∑xᵢyᵢ, a scalar. Element-wise would be <code>x*y</code>; outer product is <code>np.outer</code>. <code>@</code> is valid Python syntax, so no SyntaxError.
</div>

---
<h1 id="week2" style="color:#fff; background:#2e7d32; padding:16px; border-radius:12px;">🟩 WEEK 2 — Machine Learning with Scikit-learn</h1>

<p style="color:#555;"><b>Topics:</b> regression · classification · clustering · pipelines · hyperparameter tuning · evaluation metrics · encoders</p>

<h2 style="color:#2e7d32;">📖 NOTES</h2>

<h3 style="color:#1b5e20;">1. The estimator API (the pattern behind everything)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
model.fit(X, y)          # learn parameters
model.predict(X)         # class / value predictions
model.predict_proba(X)   # class probabilities (classifiers)
model.score(X, y)        # default metric (R² for reg, accuracy for clf)
model.transform(X)       # for transformers (scalers, encoders, PCA)
model.fit_transform(X)   # fit then transform in one call
</pre>

<b>Common models</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from sklearn.linear_model import LinearRegression, LogisticRegression, Ridge, Lasso
from sklearn.tree import DecisionTreeClassifier, DecisionTreeRegressor
from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier
from sklearn.svm import SVC
from sklearn.neighbors import KNeighborsClassifier
from sklearn.cluster import KMeans           # unsupervised
</pre>

<h3 style="color:#1b5e20;">2. Train/test split &amp; cross-validation</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from sklearn.model_selection import train_test_split, cross_val_score, GridSearchCV
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)   # random_state -> reproducible split
</pre>

<h3 style="color:#1b5e20;">3. Hyperparameter tuning — GridSearchCV</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
grid = GridSearchCV(estimator=dt, param_grid=param_grid,
                    cv=4, scoring='accuracy')
grid.fit(X_train, y_train)
grid.best_params_     # best hyperparameter combination
grid.best_score_      # best mean CV score
grid.best_estimator_  # refit model with best params
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧮 Counting fits in GridSearchCV:</b><br>
<b># combinations</b> = product of the sizes of every list in <code>param_grid</code>.<br>
<b># models trained</b> = (# combinations) × <b>cv folds</b> (+1 final refit on best params).<br>
Example: <code>max_depth:[3,5,10]</code> (3) × <code>min_samples_split:[2,5]</code> (2) × <code>criterion:['gini','entropy']</code> (2) = <b>12 combinations</b>; with <code>cv=4</code> → 12×4 = <b>48 model fits</b>.
</div>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Wording matters:</b> "48 <b>models trained</b>" is TRUE (12×4). "48 different <b>hyperparameter combinations</b> evaluated" is FALSE — there are only 12 combinations. Also, best_params_ is best on the <b>cross-validation folds</b>, not guaranteed best on X_test. Changing <code>scoring</code> (e.g. to <code>'f1'</code>) can change best_params_.
</div>

<h3 style="color:#1b5e20;">4. Classification metrics (memorise the confusion matrix)</h3>
For a class, with TP/FP/FN/TN:
<table style="border-collapse:collapse;">
<tr style="background:#e8f5e9;"><th style="padding:6px;border:1px solid #a5d6a7;">Metric</th><th style="padding:6px;border:1px solid #a5d6a7;">Formula</th><th style="padding:6px;border:1px solid #a5d6a7;">Reads as</th></tr>
<tr><td style="padding:6px;border:1px solid #a5d6a7;"><b>Precision</b></td><td style="padding:6px;border:1px solid #a5d6a7;">TP / (TP + FP)</td><td style="padding:6px;border:1px solid #a5d6a7;">of predicted-positive, how many correct</td></tr>
<tr><td style="padding:6px;border:1px solid #a5d6a7;"><b>Recall</b> (sensitivity)</td><td style="padding:6px;border:1px solid #a5d6a7;">TP / (TP + FN)</td><td style="padding:6px;border:1px solid #a5d6a7;">of actual-positive, how many found</td></tr>
<tr><td style="padding:6px;border:1px solid #a5d6a7;"><b>F1</b></td><td style="padding:6px;border:1px solid #a5d6a7;">2·P·R / (P + R)</td><td style="padding:6px;border:1px solid #a5d6a7;">harmonic mean of P &amp; R</td></tr>
<tr><td style="padding:6px;border:1px solid #a5d6a7;"><b>Accuracy</b></td><td style="padding:6px;border:1px solid #a5d6a7;">(TP+TN)/all</td><td style="padding:6px;border:1px solid #a5d6a7;">overall fraction correct</td></tr>
</table>

<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>📐 Reading a confusion matrix (rows = actual, cols = predicted):</b><br>
For class B: <b>TP</b> = cell (B,B). <b>FP</b> = other actual rows predicted as B (the B <i>column</i> minus TP). <b>FN</b> = B row minus TP (actual B predicted as something else).
</div>

<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from sklearn.metrics import (accuracy_score, precision_score, recall_score,
                             f1_score, confusion_matrix, classification_report)
recall_score(y_true, y_pred, average=None)   # per-class array
classification_report(y_true, y_pred)          # P/R/F1 for all classes
</pre>

<h3 style="color:#1b5e20;">5. Regularization</h3>
Regularization adds a penalty on weight size to the loss to fight <b>overfitting</b> by reducing model complexity.
<ul>
<li><b>L2 / Ridge</b>: penalty λ∑wᵢ² — shrinks weights smoothly toward 0 but rarely exactly 0. Good for multicollinearity.</li>
<li><b>L1 / Lasso</b>: penalty λ∑|wᵢ| — can force some weights <b>exactly to 0</b> → performs feature selection.</li>
</ul>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Bias–variance:</b> Regularization <b>increases bias</b> and <b>reduces variance</b>. It <b>reduces</b> (not increases) sensitivity to small input changes. Feature selection via zeroing weights is <b>Lasso (L1)</b>, <b>not Ridge (L2)</b>.
</div>

<h3 style="color:#1b5e20;">6. Encoders &amp; ColumnTransformer (column-counting questions)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from sklearn.preprocessing import OneHotEncoder, OrdinalEncoder, StandardScaler
from sklearn.compose import ColumnTransformer

ct = ColumnTransformer(transformers=[
        ('name', OneHotEncoder(), ['col']),
     ], remainder='passthrough')  # untouched cols appended at the end
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧮 Column math:</b><br>
<b>OneHotEncoder(drop=None)</b> → one column per unique category (k categories → k columns).<br>
<b>OrdinalEncoder</b> → 1 column (integer codes), regardless of #categories.<br>
<b>remainder='passthrough'</b> → all columns not named in a transformer are kept as-is (1 col each).
</div>

<h3 style="color:#1b5e20;">7. Decision trees, entropy &amp; information gain</h3>
Entropy of a node with class proportions pᵢ: &nbsp; <b>H = −∑ pᵢ·log₂(pᵢ)</b>.
<ul>
<li>Pure node (all one class) → H = 0.</li>
<li>Two classes 50/50 → H = 1 (maximum for binary).</li>
</ul>
<b>Information Gain</b> = H(parent) − Σ (weighted average of children's entropy).
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Watch weighting:</b> The proper weighted child entropy uses fractions (|child|/|parent|). If a question asks for the raw <code>Entropy(P) − (Entropy(L)+Entropy(R))</code> with a perfect split (both children pure), then H(P)=1, H(L)=H(R)=0 → answer = 1.
</div>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 2</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1 (MSQ).</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span><br>
Which statements about regularization are true? (select all)<br>
A. Can be used when a model overfits; typically helps by reducing model complexity.<br>
B. Ridge regularization can perform feature selection as it forces some weights exactly to zero.<br>
C. Regularization adds constraints and can increase bias while reducing variance.<br>
D. Regularization increases sensitivity of the model to small input changes.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2 (MSQ).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
GridSearchCV setup: <code>max_depth:[3,5,10]</code>, <code>min_samples_split:[2,5]</code>, <code>criterion:['gini','entropy']</code>, <code>cv=4</code>. Select the true statements.<br>
A. best_params_ offers the best performance on X_test from the given choices in param_grid.<br>
B. Changing scoring to f1 can lead to a different set of hyperparameters in best_params_.<br>
C. 48 decision tree models are trained in total.<br>
D. A total of 48 different hyperparameter combinations are evaluated.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3 (SA).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Multi-class problem, classes 0/1/2.<br>
<code>y_true = [0,0,0,0,0,0,0, 1,1,1,1,1,1, 2,2,2,2,2,2,2]</code><br>
<code>y_pred = [0,0,1,0,2,0,1, 1,1,0,1,2,1, 2,1,2,0,2,2,1]</code><br>
What is the <b>recall</b> for class 1? (2 dp) — <i>Possible answer: 0.65 to 0.68</i>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4 (SA).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Confusion matrix (rows=Actual, cols=Predicted A,B,C):<br>
A: 40 5 5 &nbsp;|&nbsp; B: 10 30 10 &nbsp;|&nbsp; C: 5 5 35.<br>
Calculate <b>precision for Class B</b> (2 dp). — <i>Possible answer: 0.73 to 0.77</i>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5 (SA).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Parent P: 50 class-A + 50 class-B (100 total). After split, left child L = 50 class-B, right child R = 50 class-A. What is the absolute value of <code>Entropy(P) − (Entropy(L) + Entropy(R))</code>? — <i>Possible answer: 1</i>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6 (SA).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Dataset df: 20000 rows, 7 columns (id, road_type, num_lanes, weather, speed_limit, area, public). Unique counts: road_type-4, weather-3, area-30, others as given. After <code>df.drop(columns=['id'])</code> then a ColumnTransformer with OneHot on road_type &amp; weather, Ordinal on area, <code>remainder='passthrough'</code>. How many columns in <code>X_encoded</code>? — <i>Possible answer: 11</i>
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 2</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → A and C.</b> A is the classic use of regularization. C correctly states the bias↑/variance↓ trade-off. B is false — <b>Lasso (L1)</b>, not Ridge (L2), zeroes weights. D is false — regularization <i>reduces</i> sensitivity.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → B and C.</b> Combinations = 3×2×2 = 12; models trained = 12×4 = <b>48</b> (C true). D is false (only 12 combinations, not 48). A is false — best_params_ is best on the CV folds, not on the held-out X_test. B is true — a different scoring metric can select different hyperparameters.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → 0.67.</b> Recall(1) = TP/(actual 1s). There are 6 actual 1s (positions in the middle block <code>1,1,0,1,2,1</code>). Predicted correctly as 1: the 1st, 2nd, 4th, 6th → 4 correct; the 3rd predicted 0, the 5th predicted 2. Recall = 4/6 = <b>0.6667 ≈ 0.67</b> ✅ (within 0.65–0.68).
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → 0.75.</b> Precision(B) = TP_B / (all predicted B). Predicted-B column = A→B (5) + B→B (30) + C→B (5) = 40. TP_B = 30. Precision = 30/40 = <b>0.75</b> ✅.
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → 1.</b> H(P): 50/50 split → −(0.5·log₂0.5 + 0.5·log₂0.5) = 1. L is pure (all B) → H=0; R is pure (all A) → H=0. So |1 − (0+0)| = <b>1</b>. (The split is perfect — maximal information gain.)
</div>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → 11.</b> Drop id → 6 columns remain. OneHot(road_type, 4 cats)=4; OneHot(weather, 3 cats)=3; Ordinal(area)=1; passthrough columns = the remaining untouched ones: num_lanes, speed_limit, public = 3. Total = 4+3+1+3 = <b>11</b> ✅. (Note: area's 30 unique values still give only 1 ordinal column.)
</div>

---
<h1 id="week3" style="color:#fff; background:#c62828; padding:16px; border-radius:12px;">🟥 WEEK 3 — Deep Learning with PyTorch &amp; TensorFlow</h1>

<p style="color:#555;"><b>Topics:</b> tensors · autograd · the training loop · custom Datasets/DataLoaders · GPU training · save/load</p>

<h2 style="color:#c62828;">📖 NOTES</h2>

<h3 style="color:#b71c1c;">1. Tensors</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import torch
torch.tensor([1,2,3])          torch.zeros(2,3)      torch.ones(2,3)
torch.from_numpy(np_array)     t.numpy()             # NumPy <-> tensor bridge
t.shape   t.dtype   t.device
t.view(2,5)  t.reshape(2,5)    # reshape; view needs contiguous memory
t.to('cuda')                   # move tensor to GPU (returns a NEW tensor)
t.to('cpu')                    t.cuda()   t.cpu()
torch.cuda.is_available()      # check for a GPU
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ <code>x = x.to('cuda')</code></b> moves tensor <code>x</code> onto the GPU for computation. It does <b>not</b> copy to CPU, does <b>not</b> change dtype, and does <b>not</b> enable mixed precision. The reassignment is required because <code>.to()</code> returns a new tensor.
</div>

<h3 style="color:#b71c1c;">2. Autograd — gradients</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
w = torch.tensor(2.0, requires_grad=True)   # track ops for this tensor
loss.backward()      # compute d(loss)/d(param) -> fills each param.grad
w.grad               # the accumulated gradient
with torch.no_grad(): ...   # disable grad tracking (inference / eval)
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧠 Gradient accumulation is the DEFAULT behaviour:</b> <code>loss.backward()</code> <b>adds</b> the new gradients to the existing <code>.grad</code> attributes rather than replacing them. That is why you must call <code>optimizer.zero_grad()</code> each step — otherwise gradients from previous batches pile up.
</div>
<ul>
<li>To <b>accumulate</b> across N mini-batches: call <code>backward()</code> N times, step once, then zero — i.e. <b>do NOT</b> zero after every backward.</li>
<li><code>loss.backward()</code> does <b>not</b> auto-clear old gradients. Clearing is <code>optimizer.zero_grad()</code> (or <code>model.zero_grad()</code>).</li>
<li>Gradient accumulation is <b>not</b> "enabled" by <code>requires_grad=True</code> — that flag only turns on tracking for a tensor.</li>
</ul>

<h3 style="color:#b71c1c;">3. THE TRAINING LOOP (learn this cold — it is tested every term)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
for epoch in range(num_epochs):
    for inputs, labels in dataloader:      # (C) iterate batches
        optimizer.zero_grad()              # (E) clear old gradients   [Step 1 / Line A]
        outputs = model(inputs)            # (A) forward pass
        loss = criterion(outputs, labels)  #     compute loss
        loss.backward()                    # (D) backprop -> grads      [Step 2 / Line B]
        optimizer.step()                   # (B) update weights         [Step 3 / Line C]
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>✅ Canonical order:</b> <code>zero_grad()</code> → <code>forward</code> → <code>loss</code> → <code>loss.backward()</code> → <code>optimizer.step()</code>.<br>
Using the block labels: <b>(C) → (E) → (A) → (D) → (B)</b>.<br>
For the "3 missing lines A, B, C" question the answer is <b>A: optimizer.zero_grad()</b>, <b>B: loss.backward()</b>, <b>C: optimizer.step()</b>.
</div>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Why this order?</b> You must clear stale grads <i>before</i> the forward, compute the loss, backprop to fill <code>.grad</code>, then step to apply them. Stepping before backward, or backward before forward, breaks training.
</div>

<h3 style="color:#b71c1c;">4. Evaluation mode &amp; disabling gradients</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
model.eval()                 # switches BatchNorm/Dropout to eval behaviour
with torch.no_grad():        # stops autograd from building the graph
    preds = model(X_val)
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Two different jobs:</b><br>
• <code>with torch.no_grad():</code> and manually setting <code>requires_grad=False</code> both <b>stop gradient tracking</b>.<br>
• <code>model.eval()</code> changes layer <i>behaviour</i> (Dropout off, BatchNorm uses running stats) but does <b>NOT</b> stop gradient tracking on its own.<br>
• <code>optimizer.zero_grad()</code> clears gradients — it does not prevent tracking.
</div>

<h3 style="color:#b71c1c;">5. Custom Dataset &amp; DataLoader</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from torch.utils.data import Dataset, DataLoader

class MyData(Dataset):
    def __init__(self, X, y):        # setup (NOT required by DataLoader contract)
        self.X, self.y = X, y
    def __len__(self):               # REQUIRED -> number of samples
        return len(self.X)
    def __getitem__(self, idx):      # REQUIRED -> one (sample, label) pair
        return self.X[idx], self.y[idx]

loader = DataLoader(ds, batch_size=32, shuffle=True)
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>✅ A map-style Dataset MUST override <code>__getitem__</code> and <code>__len__</code>.</b> <code>__iter__</code> is only for iterable-style datasets; <code>__init__</code> is optional and not part of the DataLoader contract.
</div>

<h3 style="color:#b71c1c;">6. Building a model, loss &amp; optimizer</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import torch.nn as nn
model = nn.Sequential(nn.Linear(10, 32), nn.ReLU(), nn.Linear(32, 1))
criterion = nn.CrossEntropyLoss()      # classification
criterion = nn.MSELoss()               # regression
optimizer = torch.optim.Adam(model.parameters(), lr=1e-3)
</pre>

<h3 style="color:#b71c1c;">7. Save / load &amp; GPU</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
torch.save(model.state_dict(), 'model.pt')          # recommended
model.load_state_dict(torch.load('model.pt'))
model.eval()

device = 'cuda' if torch.cuda.is_available() else 'cpu'
model.to(device); inputs = inputs.to(device); labels = labels.to(device)
</pre>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 3</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span> <i>(training-loop order appears in BOTH papers)</i><br>
Training loop with three missing lines (Step1=A, Step2=B, Step3=C) between <code>loss = criterion(...)</code> being computed. Which fills A, B, C in order?<br>
A: <code>optimizer.zero_grad()</code>; B: <code>loss.backward()</code>; C: <code>optimizer.step()</code><br>
(other options permute these three)
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span> <i>(same theme, kept as a deliberate duplicate)</i><br>
Arrange the blocks into a valid one-epoch training loop:<br>
(A) <code>outputs=model(inputs); loss=criterion(outputs,labels)</code> (B) <code>optimizer.step()</code> (C) <code>for inputs,labels in dataloader:</code> (D) <code>loss.backward()</code> (E) <code>optimizer.zero_grad()</code><br>
Options: 1) C→E→A→D→B &nbsp; 2) C→B→E→A→D &nbsp; 3) E→C→A→B→D &nbsp; 4) C→E→A→B→D
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3 (MSQ).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Which snippets correctly prevent PyTorch from tracking gradients during evaluation? (select all)<br>
A. Wrapping the code in <code>with torch.no_grad():</code><br>
B. Setting <code>requires_grad=False</code> on the model parameters manually<br>
C. Calling <code>optimizer.zero_grad()</code> before the forward pass<br>
D. Calling <code>model.eval()</code> before passing validation data
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4 (MSQ).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
When inheriting from <code>torch.utils.data.Dataset</code>, which methods must be overridden for <code>DataLoader</code> compatibility? (select all)<br>
A. <code>__getitem__</code> &nbsp; B. <code>__iter__</code> &nbsp; C. <code>__len__</code> &nbsp; D. <code>__init__</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
When performing gradient accumulation in PyTorch, which statements are true?<br>
A. Gradients from <code>loss.backward()</code> are <b>added</b> to existing <code>.grad</code> rather than replacing them.<br>
B. To accumulate over multiple mini-batches you must call <code>optimizer.zero_grad()</code> after every <code>loss.backward()</code>.<br>
C. Calling <code>loss.backward()</code> automatically clears previously stored gradients.<br>
D. Gradient accumulation is enabled by setting <code>requires_grad=True</code>.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
What does <code>x = x.to('cuda')</code> do?<br>
A. Moves tensor x to the GPU for computation &nbsp; B. Creates a copy of x on CPU &nbsp; C. Converts x to a CUDA integer type &nbsp; D. Enables mixed-precision computation
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 3</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → A: zero_grad(), B: backward(), C: step().</b> Clear stale grads → backprop the loss → update weights. Any other order (step before backward, etc.) breaks learning.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → Option 1: C → E → A → D → B.</b> Loop over batches (C), zero grads (E), forward+loss (A), backward (D), step (B).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → A and B.</b> Both actually stop gradient tracking. <code>model.eval()</code> (D) only changes Dropout/BatchNorm behaviour, it does not stop tracking. <code>zero_grad()</code> (C) merely clears grads.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → A and C.</b> A map-style Dataset must implement <code>__getitem__</code> and <code>__len__</code>. <code>__iter__</code> is for iterable-style datasets; <code>__init__</code> is optional.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → A only.</b> A is the definition of accumulation. B is false — to accumulate you must <i>not</i> zero after every backward (zero only once per optimizer step). C is false — backward accumulates, it doesn't clear. D is false — <code>requires_grad</code> just enables tracking.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → A.</b> <code>.to('cuda')</code> returns a GPU-resident copy of the tensor for computation.
</div>

---
<h1 id="week4" style="color:#fff; background:#ef6c00; padding:16px; border-radius:12px;">🟧 WEEK 4 — Computer Vision &amp; Image Processing</h1>

<p style="color:#555;"><b>Tools:</b> OpenCV (cv2) · PIL/Pillow · CNNs · Transfer Learning (ResNet, MobileNet) · YOLO</p>

<h2 style="color:#ef6c00;">📖 NOTES</h2>

<h3 style="color:#e65100;">1. How images are represented</h3>
<ul>
<li><b>Grayscale, 8-bit:</b> a 2-D array <code>(Height, Width)</code>, pixel values <b>0–255</b>. <b>0 = pure black, 255 = pure white.</b></li>
<li><b>Color (RGB):</b> a 3-D array with shape <b><code>(Height, Width, 3)</code></b> — the 3 is the channel axis, last.</li>
</ul>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Channel order convention:</b><br>
• <b>PIL / Pillow</b> loads color images as <b>RGB</b>.<br>
• <b>OpenCV (cv2)</b> loads color images as <b>BGR</b> (blue and red swapped!). Convert with <code>cv2.cvtColor(img, cv2.COLOR_BGR2RGB)</code>.<br>
Both ultimately give <code>(H, W, 3)</code> arrays — the difference is the <i>channel order</i>, not the format.
</div>

<h3 style="color:#e65100;">2. Loading &amp; manipulating images</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
# --- OpenCV ---
import cv2
img = cv2.imread("sample.jpg")           # BGR, shape (H, W, 3)
resized = cv2.resize(img, (W_new, H_new))# NOTE: size is (width, height)!
cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)    # to grayscale
cv2.imwrite("out.jpg", img)

# --- Pillow ---
from PIL import Image
im = Image.open("sample.jpg")            # RGB
im = im.resize((W_new, H_new))
im = im.convert("L")                     # grayscale
import numpy as np; arr = np.array(im)   # PIL -> NumPy
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧮 <code>cv2.resize</code> behaviour:</b> resizing a <code>(300, 600, 3)</code> image with <code>cv2.resize(img, (200,200))</code> succeeds and produces a <code>(200, 200, 3)</code> array — the <b>channel count is preserved</b> (still 3, not 1). Resizing does <b>not</b> require dimensions to match the original, and you don't specify channels. The new aspect ratio is 200:200 = <b>1:1</b>.
</div>

<h3 style="color:#e65100;">3. The four core Computer-Vision tasks</h3>
<table style="border-collapse:collapse;">
<tr style="background:#fff3e0;"><th style="padding:6px;border:1px solid #ffcc80;">Task</th><th style="padding:6px;border:1px solid #ffcc80;">Output</th></tr>
<tr><td style="padding:6px;border:1px solid #ffcc80;"><b>Image Classification</b></td><td style="padding:6px;border:1px solid #ffcc80;">One label for the whole image ("School Zone").</td></tr>
<tr><td style="padding:6px;border:1px solid #ffcc80;"><b>Object Detection</b></td><td style="padding:6px;border:1px solid #ffcc80;">Class + bounding box (x,y,w,h) per object ("Pedestrian at [50,100]").</td></tr>
<tr><td style="padding:6px;border:1px solid #ffcc80;"><b>Instance Segmentation</b></td><td style="padding:6px;border:1px solid #ffcc80;">Separate pixel mask per <i>object instance</i> (each cyclist masked individually).</td></tr>
<tr><td style="padding:6px;border:1px solid #ffcc80;"><b>Semantic Segmentation</b></td><td style="padding:6px;border:1px solid #ffcc80;">A class label for <i>every pixel</i> (40% Road, 30% Building, …), no instance separation.</td></tr>
</table>

<h3 style="color:#e65100;">4. YOLO &amp; Non-Maximum Suppression (NMS)</h3>
YOLO ("You Only Look Once") predicts many candidate boxes in one pass; each has a confidence score. <b>NMS</b> removes duplicate detections of the same object:
<ol>
<li>Pick the box with the <b>highest confidence score</b>.</li>
<li>Suppress (remove) all remaining boxes whose <b>IoU overlap</b> with it exceeds a threshold.</li>
<li>Repeat on the remaining boxes.</li>
</ol>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ NMS does NOT</b> average coordinates, merge boxes recursively, or maximise scores of distant boxes. It <i>selects the best and suppresses high-overlap rivals</i>.
</div>

<h3 style="color:#e65100;">5. Data Augmentation</h3>
Creating modified copies of training images (rotation, flip, scaling, cropping, colour jitter…) to <b>artificially expand the dataset</b>, help the model <b>generalize</b> to unseen data, and <b>reduce overfitting</b>.
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Augmentation is NOT</b> about making images smaller for speed, nor about denoising/grayscale conversion. Those are preprocessing, not augmentation.
</div>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from torchvision import transforms
transforms.Compose([
    transforms.RandomHorizontalFlip(),
    transforms.RandomRotation(15),
    transforms.Resize((224,224)),
    transforms.ToTensor(),
    transforms.Normalize(mean=[...], std=[...]),
])
</pre>

<h3 style="color:#e65100;">6. Transfer learning (ResNet / MobileNet)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
import torchvision.models as models
resnet = models.resnet18(weights='IMAGENET1K_V1')  # pretrained backbone
for p in resnet.parameters(): p.requires_grad = False   # freeze
resnet.fc = nn.Linear(resnet.fc.in_features, num_classes)  # new head
</pre>
Idea: reuse features learned on ImageNet, replace &amp; train only the final classifier head for your task.

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 4</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Match CV Task → Output. 1=Image Classification, 2=Object Detection, 3=Instance Segmentation, 4=Semantic Segmentation. A=every pixel labelled by class%, B=pedestrian/traffic-light in boxes, C=whole scene = "School Zone", D=separate pixel-mask per cyclist.<br>
Options: (i) 1-C;2-D;3-A;4-B &nbsp; (ii) 1-C;2-B;3-A;4-D &nbsp; (iii) 1-C;2-B;3-D;4-A &nbsp; (iv) 1-C;2-D;3-B;4-A
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Which best describes Non-Maximum Suppression in YOLO?<br>
A. Averages coordinates of all overlapping boxes into one refined box.<br>
B. Selects the box with the highest confidence and suppresses remaining boxes with high overlap.<br>
C. Maximises confidence of distant boxes while suppressing overlapping ones.<br>
D. Recursively merges overlapping boxes by taking higher coordinates.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3 (MSQ — pick the FALSE ones).</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Image <code>(300,600,3)</code> processed by <code>resized = cv2.resize(img,(200,200))</code>. Which statements are <b>False</b>?<br>
A. The operation fails because target W/H don't match original dimensions.<br>
B. The operation fails because channels aren't specified while resizing.<br>
C. <code>resized.shape</code> will be <code>(200,200,1)</code>.<br>
D. The new aspect ratio of the resized image is 1:1.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
In a standard 8-bit grayscale image, what values represent pure black and pure white?<br>
A. 0 black, 255 white &nbsp; B. 255 black, 0 white &nbsp; C. 0 black, 1 white &nbsp; D. -1 black, 1 white
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
How is a standard color (RGB) image typically represented as a NumPy array?<br>
A. 1D vector &nbsp; B. 2D (Height, Width) &nbsp; C. 3D (3, Height, Width) &nbsp; D. 3D (Height, Width, 3)
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Which statements about Data Augmentation are correct?<br>
A. Involves modified copies via rotation, scaling, cropping, etc.<br>
B. Artificially expands the dataset to generalize better and reduce overfitting.<br>
C. Primary objective is to make images smaller for faster training.<br>
D. Used to remove noise and convert to grayscale.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q7.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Main difference between <code>PIL.Image.open()</code> and <code>cv2.imread()</code> for a color image?<br>
A. Pillow loads as NumPy array, OpenCV in a custom format.<br>
B. Pillow loads in RGB, OpenCV in BGR.
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 4</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → (ii) 1-C; 2-B; 3-D; 4-A.</b> Classification→whole-scene label (C); Detection→boxes (B); Instance seg→per-instance masks per cyclist (D); Semantic seg→every pixel labelled by class percentage (A).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → B.</b> NMS keeps the highest-confidence box and suppresses others that overlap it heavily (high IoU).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → A, B, C are False</b> (the "correct" selections). Resize succeeds regardless of original size (A false) and without specifying channels (B false); the result keeps 3 channels so shape is <code>(200,200,3)</code>, making C false. D is <b>true</b> (200:200 = 1:1), so D is not selected.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → A.</b> 8-bit grayscale ranges 0–255: 0 = black, 255 = white.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → D.</b> RGB images are <code>(Height, Width, 3)</code> — channels last in NumPy/OpenCV/PIL. (The <code>(3,H,W)</code> "channels-first" form is what PyTorch tensors use internally, but the standard NumPy image is channels-last.)
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → A and B.</b> Those define augmentation. C (shrinking for speed) and D (denoise/grayscale) are preprocessing, not augmentation.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q7 → B.</b> Pillow → RGB, OpenCV → BGR. (Both can become NumPy arrays, so A is wrong.)
</div>

---
<h1 id="week5" style="color:#fff; background:#6a1b9a; padding:16px; border-radius:12px;">🟪 WEEK 5 — NLP &amp; LLMs using HuggingFace</h1>

<p style="color:#555;"><b>Topics:</b> Transformers · Tokenization · 🤗 Datasets · Fine-tuning (BERT/RoBERTa/GPT-2) · LoRA/PEFT · text generation</p>

<h2 style="color:#6a1b9a;">📖 NOTES</h2>

<h3 style="color:#4a148c;">1. Tokenizers</h3>
A tokenizer converts text → token IDs the model can read, adding special tokens and handling padding/truncation.
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from transformers import AutoTokenizer
tok = AutoTokenizer.from_pretrained("bert-base-uncased")

out = tok(sentences,
          padding=True,           # pad shorter seqs to the longest in batch
          truncation=True,        # cut seqs longer than max_length
          max_length=6,           # cap length at 6 tokens
          return_tensors="pt")    # "pt"=PyTorch, "tf"=TF, "np"=NumPy
out["input_ids"]        out["attention_mask"]
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧠 padding + truncation + max_length together:</b> every sequence is forced to <b>exactly max_length</b> — short ones padded up, long ones cut down. So all rows of <code>input_ids</code> share the same length (e.g. 6). Special tokens <code>[CLS]</code>/<code>[SEP]</code> <b>are still added</b> (padding doesn't disable them). With <code>return_tensors="pt"</code> you get tensors, not Python lists.
</div>

<h3 style="color:#4a148c;">2. Models &amp; inference</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from transformers import AutoModelForSequenceClassification, AutoModelForCausalLM, pipeline
model = AutoModelForSequenceClassification.from_pretrained("bert-base-uncased", num_labels=2)
clf = pipeline("sentiment-analysis")          # quick inference
gen = pipeline("text-generation", model="gpt2")
</pre>

<h3 style="color:#4a148c;">3. Text-generation decoding parameters</h3>
<table style="border-collapse:collapse;">
<tr style="background:#f3e5f5;"><th style="padding:6px;border:1px solid #ce93d8;">Param</th><th style="padding:6px;border:1px solid #ce93d8;">Effect</th></tr>
<tr><td style="padding:6px;border:1px solid #ce93d8;"><b>temperature</b></td><td style="padding:6px;border:1px solid #ce93d8;">Higher → flattens the probability distribution → more randomness/creativity. Lower (→0) → sharper → deterministic, repetitive.</td></tr>
<tr><td style="padding:6px;border:1px solid #ce93d8;"><b>top_k</b></td><td style="padding:6px;border:1px solid #ce93d8;">Sample only from the k highest-probability tokens.</td></tr>
<tr><td style="padding:6px;border:1px solid #ce93d8;"><b>top_p</b> (nucleus)</td><td style="padding:6px;border:1px solid #ce93d8;">Sample from the smallest set whose cumulative prob ≥ p.</td></tr>
</table>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Temperature mnemonic:</b> <b>high temperature = high randomness</b> (less-likely words become more probable). It does NOT limit vocabulary size (that's top_k) or penalise n-gram repeats.
</div>

<h3 style="color:#4a148c;">4. 🤗 Datasets library</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from datasets import load_dataset, concatenate_datasets
ds = load_dataset("imdb", split="train")
ds = load_dataset("csv", data_files="reviews.csv")

ds.select(range(0, 500, 10))   # pick indices 0,10,20,...,490 -> 50 rows
                               # returns a NEW Dataset; original UNCHANGED
ds.map(fn)                     # apply fn to each example, returns new Dataset
ds.filter(fn)   ds.shuffle()   ds.train_test_split(test_size=0.2)
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧮 <code>.select(range(0,500,10))</code></b> → indices 0,10,…,490 = <b>50 samples</b>. It returns a new Dataset of type <code>Dataset</code>; the original is <b>not modified</b>.
</div>

<b>Adding a column with <code>.map()</code></b> — two valid patterns:
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
# (a) return a dict of the NEW column(s):
def add_len(ex): return {"char_count": len(ex["text"])}
ds = ds.map(add_len)

# (b) mutate the example dict and return it:
def add_len(ex):
    ex["char_count"] = len(ex["text"]); return ex
ds = ds.map(add_len)
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Pandas-style writes do NOT work on a 🤗 Dataset:</b> <code>dataset["col"] = ...</code> and <code>dataset.add_column("c", dataset["text"].apply(len))</code> are invalid (a Dataset column has no <code>.apply</code>, and item-assignment isn't supported this way).
</div>

<b>Combining datasets — <code>concatenate_datasets</code></b>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Schema must match.</b> <code>concatenate_datasets([ds1, ds2])</code> stacks rows only if both share the <b>same column names AND types</b>. If ds1 has (text, label) and ds2 has (review, sentiment), you must first align names via <code>.rename_column()</code> (or <code>.map()</code>). It does <b>not</b> auto-align columns and does <b>not</b> modify inputs in place; it does not require matching split names.
</div>

<h3 style="color:#4a148c;">5. Fine-tuning &amp; the Trainer</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from transformers import TrainingArguments, Trainer
args = TrainingArguments(output_dir="out", num_train_epochs=3,
                         per_device_train_batch_size=16, learning_rate=2e-5)
trainer = Trainer(model=model, args=args,
                  train_dataset=train_ds, eval_dataset=val_ds)
trainer.train();  trainer.evaluate()
</pre>

<h3 style="color:#4a148c;">6. LoRA / PEFT (parameter-efficient fine-tuning)</h3>
LoRA injects small trainable low-rank adapter matrices into chosen layers (named in <code>target_modules</code>) and freezes the rest — cheap fine-tuning.
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from peft import LoraConfig, get_peft_model
lora_config = LoraConfig(
    r=8, lora_alpha=16,
    target_modules=["q_proj","v_proj"],   # WHICH layers get adapters
    lora_dropout=0.1, bias="none", task_type="CAUSAL_LM")
model = get_peft_model(base_model, lora_config)
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ <code>target_modules=[]</code> (empty list)</b> → no layers are targeted, so <b>LoRA is applied to no layer</b>. It is a valid (if useless) config — no error is thrown, and it doesn't touch embeddings or a classification head.
</div>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 5</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
What happens if you set <code>target_modules=[]</code> in <code>LoraConfig</code>?<br>
A. LoRA applied to entire model incl. embeddings &nbsp; B. LoRA only on final classification layer &nbsp; C. LoRA not applied to any layer &nbsp; D. Error, empty list invalid
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Tokenizer called with <code>padding=True, truncation=True, max_length=6, return_tensors="pt"</code>. Which statement is TRUE?<br>
A. Each sentence tokenized independently without padding because max_length is specified.<br>
B. All sequences in <code>output["input_ids"]</code> will have length exactly 6.<br>
C. The tokenizer returns a list of Python integers.<br>
D. Special tokens [CLS]/[SEP] won't be added because padding is enabled.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
<code>ds = load_dataset("imdb", split="train"); sample = ds.select(range(0,500,10))</code>. Select correct statements.<br>
A. sample contains 50 samples. &nbsp; B. range(0,500,10) selects rows in steps of 10. &nbsp; C. Original dataset is modified after .select(). &nbsp; D. sample is of type Dataset.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
ds1 has columns text(str),label(int); ds2 has review(str),sentiment(int). About <code>concatenate_datasets([ds1,ds2])</code>, select correct statements.<br>
A. Combined dataset auto-aligns columns and combines rows successfully.<br>
B. You must align column names using .rename_column() or .map().<br>
C. concatenate_datasets requires both to have the same split names.<br>
D. Both datasets must have the same schema (column names and types) to be concatenated.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Add a <code>char_count</code> column (char count of <code>text</code>) using <code>.map()</code>. Which snippets work?<br>
A. <code>def f(ex): return {"char_count": len(ex["text"])}</code> ; <code>ds=ds.map(f)</code><br>
B. <code>def f(ex): ex["char_count"]=len(ex["text"]); return ex</code> ; <code>ds=ds.map(f)</code><br>
C. <code>ds = ds.add_column("char_count", ds["text"].apply(len))</code><br>
D. <code>ds["char_count"] = ds["text"].map(len)</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
In text generation with GPT-2, increasing the temperature generally…<br>
A. Makes output more deterministic and repetitive.<br>
B. Increases randomness by flattening the probability distribution, making less-likely words more probable.<br>
C. Strictly limits vocabulary size considered at each step.<br>
D. Increases penalty for repeating n-grams.
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 5</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → C.</b> No layer names → no adapters inserted. Valid config, no error.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → B.</b> padding + truncation + max_length=6 forces every sequence to length 6. Special tokens are still added (D false); output is tensors, not lists (C false); padding is applied (A false).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → A, B, D.</b> 0,10,…,490 = 50 rows (A), steps of 10 (B), result is a Dataset (D). <code>.select()</code> returns a new object; the original is untouched, so C is false.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → B and D.</b> Schemas differ, so you must rename to align (B) and both need identical column names/types to concatenate (D). It does not auto-align (A false) and doesn't need matching split names (C false).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → A and B.</b> Both the "return new dict" and "mutate-and-return" patterns are valid <code>map</code> functions. C and D use Pandas-style APIs that don't exist on a 🤗 Dataset.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → B.</b> Higher temperature flattens the softmax distribution → more randomness. It does not limit vocab (top_k) or penalise n-grams.
</div>

---
<h1 id="week6" style="color:#fff; background:#00838f; padding:16px; border-radius:12px;">🟦 WEEK 6 — Prompt Engineering, LangChain &amp; LLM APIs</h1>

<p style="color:#555;"><b>Topics:</b> prompting · LangChain core (LLMs, PromptTemplates, OutputParsers) · LCEL chains · memory · invoke/batch · OpenAI/Gemini/Ollama APIs</p>

<h2 style="color:#00838f;">📖 NOTES</h2>

<h3 style="color:#006064;">1. Prompt engineering essentials</h3>
<ul>
<li><b>Zero-shot</b>: just the instruction. <b>Few-shot</b>: instruction + examples.</li>
<li><b>Chain-of-Thought</b>: ask the model to reason step by step.</li>
<li>Best practices: be specific, give format/constraints, provide examples, set a role.</li>
</ul>

<h3 style="color:#006064;">2. LangChain chat models &amp; the determinism of temperature</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_openai import ChatOpenAI
from langchain_google_genai import ChatGoogleGenerativeAI
from langchain_groq import ChatGroq

llm = ChatOpenAI(model="gpt-3.5-turbo", temperature=0.5)
gllm = ChatGoogleGenerativeAI(model="gemini-2.5-flash", temperature=0)

llm.invoke("Hello")          # single prompt -> one response object (.content)
llm.batch([p1, p2, p3])      # list of prompts -> list of responses (same order)
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Model-name ↔ class must match:</b> <code>ChatOpenAI</code> works with OpenAI models like <code>gpt-3.5-turbo</code>. Passing <code>"gemini-2.0-flash"</code> or <code>"llama3-8b-8192"</code> into <code>ChatOpenAI</code> is invalid — those belong to Gemini / Groq clients respectively.
</div>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🎯 Determinism:</b> <code>temperature=0</code> makes sampling greedy → the <b>same prompt gives the same output</b> every run (infrastructure unchanged). <code>temperature&gt;0</code> introduces randomness → outputs can differ between runs. So among snippets differing only in temperature, the <code>temperature=0</code> one is the reproducible one.
</div>

<h3 style="color:#006064;">3. <code>invoke</code> vs <code>batch</code></h3>
<table style="border-collapse:collapse;">
<tr style="background:#e0f7fa;"><th style="padding:6px;border:1px solid #80deea;">Method</th><th style="padding:6px;border:1px solid #80deea;">Input</th><th style="padding:6px;border:1px solid #80deea;">Output</th></tr>
<tr><td style="padding:6px;border:1px solid #80deea;"><code>invoke(x)</code></td><td style="padding:6px;border:1px solid #80deea;">one input</td><td style="padding:6px;border:1px solid #80deea;">one response object</td></tr>
<tr><td style="padding:6px;border:1px solid #80deea;"><code>batch([...])</code></td><td style="padding:6px;border:1px solid #80deea;">list of inputs</td><td style="padding:6px;border:1px solid #80deea;"><b>list of response objects, same order</b> (processed in parallel)</td></tr>
<tr><td style="padding:6px;border:1px solid #80deea;"><code>stream(x)</code></td><td style="padding:6px;border:1px solid #80deea;">one input</td><td style="padding:6px;border:1px solid #80deea;">token-by-token generator</td></tr>
</table>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ <code>batch()</code> does NOT</b> merge inputs into one prompt, return a dict keyed by input, or return plain strings. It returns a <b>list of response objects in the same order as the inputs</b>.
</div>

<h3 style="color:#006064;">4. PromptTemplate + OutputParser + LCEL chains</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_core.prompts import ChatPromptTemplate
from langchain_core.output_parsers import StrOutputParser

prompt = ChatPromptTemplate.from_template("What is the capital of {country}?")
chain = prompt | ChatOpenAI() | StrOutputParser()   # LCEL: pipe components
chain.invoke({"country": "France"})   # keys MUST match the template variables
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🎯 Invoking a templated chain:</b> pass a <b>dict whose keys are the template's variables</b>. For <code>{country}</code> that is <code>chain.invoke({"country": "France"})</code>. A raw string, a wrong key ("prompt"), or a bare value won't populate <code>{country}</code>.
</div>

<h3 style="color:#006064;">5. Debugging intermediate LCEL values</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_core.runnables import RunnableLambda
# print the prompt right after it is built, before the model:
chain = prompt | RunnableLambda(print) | model
# OR run just the prompt component:
prompt.invoke(input)
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️</b> Inserting <code>RunnableLambda(print)</code> or invoking the prompt alone both expose the intermediate message efficiently. Setting <code>verbose=True</code> is broad/noisy, and "intermediate steps aren't accessible" is simply false.
</div>

<h3 style="color:#006064;">6. Memory &amp; compiling a LangGraph app (bridge to Week 8)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
# LangChain classic memory:
from langchain.memory import ConversationBufferMemory
# LangGraph build/run pattern (used in Week 8):
app = graph.compile()                 # compile the graph into a runnable
output = app.invoke({"query": "..."}) # run it
</pre>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 6</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
<code>responses = llm.batch(inputs)</code> where inputs is a list of 3 prompts. Which describes the behaviour?<br>
A. Merges all inputs into one prompt, returns a single string.<br>
B. Processes all inputs in a single batch request and returns a list of response objects in the same order as inputs.<br>
C. Returns a dictionary mapping each input to its response.<br>
D. Runs each input sequentially like a for-loop with invoke() and returns plain strings.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Which snippet runs successfully (all installs/keys/access fine)?<br>
A. <code>ChatOpenAI(model="llama3-8b-8192", temperature=0.5)</code><br>
B. <code>ChatOpenAI(model="gemini-2.0-flash", temperature=0.5)</code><br>
C. <code>ChatOpenAI(model="gpt-3.5-turbo", temperature=0.5)</code><br>
D. None of these
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Which code snippet produces the <b>same output every run</b> (model/infra unchanged)?<br>
A. ChatGoogleGenerativeAI(model="gemini-2.5-flash", <b>temperature=0</b>) → invoke(prompt)<br>
B. same but temperature=0.5 &nbsp; C. "Output cannot be same if run multiple times." &nbsp; D. temperature=1
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
<code>prompt = ChatPromptTemplate.from_template("What is the capital of {country}?")</code>; <code>chain = prompt | ChatOpenAI() | StrOutputParser()</code>. Most correct way to invoke?<br>
A. <code>chain.invoke({"prompt": "What is the capital of France?"})</code><br>
B. <code>chain.invoke("What is the capital of France")</code><br>
C. <code>chain.invoke("France")</code><br>
D. <code>chain.invoke({"country": "France"})</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
Chain <code>chain = prompt | model</code>. Most efficient ways to debug the intermediate prompt message before it hits the model? (select all)<br>
A. Add <code>RunnableLambda(print)</code> after the prompt: <code>prompt | RunnableLambda(print) | model</code>.<br>
B. Set <code>verbose=True</code> on the model.<br>
C. Use <code>print(chain.invoke(input))</code> and check final output (intermediate not accessible).<br>
D. Invoke the prompt component directly: <code>prompt.invoke(input)</code>.
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 6</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → B.</b> <code>batch()</code> sends inputs together and returns a list of response objects in input order.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → C.</b> <code>gpt-3.5-turbo</code> is a valid OpenAI model for <code>ChatOpenAI</code>. The llama and gemini names belong to Groq/Gemini clients, not OpenAI.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → A.</b> <code>temperature=0</code> → greedy/deterministic → identical output each run. Non-zero temperatures introduce randomness.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → D.</b> The template variable is <code>{country}</code>, so pass <code>{"country": "France"}</code>. Wrong key ("prompt"), bare strings won't fill the variable.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → A and D.</b> Both expose the intermediate prompt cheaply. <code>verbose=True</code> is coarse; C's premise (intermediate not accessible) is false.
</div>

---
<h1 id="week7" style="color:#fff; background:#283593; padding:16px; border-radius:12px;">🟦 WEEK 7 — Retrieval-Augmented Generation (RAG) &amp; Vector DBs</h1>

<p style="color:#555;"><b>Topics:</b> embeddings &amp; semantic search · chunking · FAISS / Pinecone / ChromaDB · retrievers · the RAG pipeline · RAG vs Fine-tuning</p>

<h2 style="color:#283593;">📖 NOTES</h2>

<h3 style="color:#1a237e;">1. Why RAG? RAG vs Fine-tuning</h3>
<b>RAG</b> = retrieve relevant documents at query time and feed them to the LLM as context, so answers are grounded in your data and <b>hallucination is minimized</b>. Great when answers must come strictly from internal documents (e.g. a legal chatbot over case files).
<table style="border-collapse:collapse;">
<tr style="background:#e8eaf6;"><th style="padding:6px;border:1px solid #9fa8da;"> </th><th style="padding:6px;border:1px solid #9fa8da;">RAG</th><th style="padding:6px;border:1px solid #9fa8da;">Fine-tuning</th></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>Analogy</b></td><td style="padding:6px;border:1px solid #9fa8da;">Googling before answering (look it up now)</td><td style="padding:6px;border:1px solid #9fa8da;">Learning permanently (bake knowledge into weights)</td></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>Updates</b></td><td style="padding:6px;border:1px solid #9fa8da;">Just change the documents</td><td style="padding:6px;border:1px solid #9fa8da;">Retrain</td></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>Best for</b></td><td style="padding:6px;border:1px solid #9fa8da;">Grounding on private/fresh docs, low hallucination</td><td style="padding:6px;border:1px solid #9fa8da;">Changing style/behaviour, domain adaptation</td></tr>
</table>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🎯 Memory hook:</b> <b>RAG = Googling before answering; Fine-tuning = learning permanently.</b> For "answer strictly from internal documents &amp; minimize hallucination" → choose <b>RAG</b>.
</div>

<h3 style="color:#1a237e;">2. Embeddings &amp; semantic search</h3>
An embedding maps text → a dense vector so that semantically similar texts are close (usually by <b>cosine similarity</b>). Semantic search = embed the query, find nearest document vectors.
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_openai import OpenAIEmbeddings
emb = OpenAIEmbeddings()
vec = emb.embed_query("some text")
</pre>

<h3 style="color:#1a237e;">3. Chunking — splitting documents</h3>
Documents are split into overlapping chunks before embedding. Overlap preserves context across boundaries.
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_text_splitters import RecursiveCharacterTextSplitter
splitter = RecursiveCharacterTextSplitter(chunk_size=300, chunk_overlap=50)
chunks = splitter.split_documents(docs)   # for Document objects
chunks = splitter.split_text(text)        # for a raw string
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Tuning for retrieval quality:</b><br>
• <b>Smaller chunk_size</b> → more focused chunks (better precision when results are irrelevant/too broad).<br>
• <b>Larger chunk_size</b> or <b>larger k</b> → more context per query.<br>
• For <b>multi-document synthesis</b> (answer spread across many docs), the most direct fix is to <b>increase k</b> so the retriever returns more chunks to combine.
</div>

<h3 style="color:#1a237e;">4. Vector stores &amp; retrievers</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langchain_community.vectorstores import FAISS, Chroma
vectorstore = FAISS.from_documents(chunks, embedding_model)

# similarity_search returns a LIST of Document objects:
results = vectorstore.similarity_search("product launch", k=3)
type(results[0])   # -> langchain_core.documents.Document

# turn a store into a retriever; control #results via search_kwargs:
retriever = vectorstore.as_retriever(search_kwargs={"k": 2})
</pre>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🎯 Controlling how many chunks come back:</b> the <b>only</b> correct way is <code>as_retriever(search_kwargs={"k": 2})</code>. Setting <code>retriever.k = 2</code> or passing <code>k=2</code> directly to <code>as_retriever(...)</code> does <b>not</b> work.
</div>
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧠 Return type:</b> <code>similarity_search(...)</code> returns a Python <b>list</b> of <b><code>Document</code></b> objects — so <code>type(results[0])</code> is <code>&lt;class 'langchain_core.documents.Document'&gt;</code>, not str/list/ndarray.
</div>

<h3 style="color:#1a237e;">5. The full RAG chain (LCEL)</h3>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
rag_chain = (
    {"context": retriever | format_docs, "question": RunnablePassthrough()}
    | prompt | llm | StrOutputParser()
)
</pre>
Fixing a RAG system that returns <b>irrelevant results</b>: increase <code>k</code>, reduce <code>chunk_size</code> for more focused chunks; removing overlap usually hurts (loses boundary context).

<h3 style="color:#1a237e;">6. Vector DB options</h3>
<table style="border-collapse:collapse;">
<tr style="background:#e8eaf6;"><th style="padding:6px;border:1px solid #9fa8da;">DB</th><th style="padding:6px;border:1px solid #9fa8da;">Nature</th></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>FAISS</b></td><td style="padding:6px;border:1px solid #9fa8da;">Local, in-memory library (Facebook AI); fast, no server.</td></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>ChromaDB</b></td><td style="padding:6px;border:1px solid #9fa8da;">Local/embedded, persistent, easy for dev.</td></tr>
<tr><td style="padding:6px;border:1px solid #9fa8da;"><b>Pinecone</b></td><td style="padding:6px;border:1px solid #9fa8da;">Managed cloud vector DB, scalable.</td></tr>
</table>

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 7</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span><br>
A legal chatbot must answer strictly from internal case documents and minimize hallucination. Which approach is MOST suitable?<br>
A. Fine-tuning &nbsp; B. RAG &nbsp; C. Temperature=0 &nbsp; D. Temperature=1 &nbsp; E. Top-p=1 &nbsp; F. Top-k=1
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Which analogy best describes RAG vs Fine-Tuning?<br>
A. RAG = memorizing textbook, Fine-tuning = Googling<br>
B. RAG = Googling before answering, Fine-tuning = learning permanently<br>
C. RAG = increasing IQ, Fine-tuning = reading newspaper
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
A developer wants only the top 2 most relevant chunks. Which is correct?<br>
A. <code>retriever = vectorstore.as_retriever()</code> then <code>retriever.k = 2</code><br>
B. <code>retriever = vectorstore.as_retriever(search_kwargs={"k": 2})</code><br>
C. <code>retriever = vectorstore.as_retriever(k=2)</code><br>
D. None of these
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
A RAG system answers direct questions well but struggles when the answer needs info spread across multiple documents (chunk_size=300, overlap=50, k=2). Which single change MOST directly improves multi-document synthesis?<br>
A. Decrease chunk_size &nbsp; B. Increase chunk_size &nbsp; C. Increase chunk_overlap &nbsp; D. Increase k
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
<code>results = vectorstore.similarity_search("product launch", k=3); print(type(results[0]))</code> retrieves what type?<br>
A. <code>langchain_core.documents.Document</code> &nbsp; B. <code>str</code> &nbsp; C. <code>list</code> &nbsp; D. <code>numpy.ndarray</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6 (MSQ).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
RAG returns irrelevant results (chunk_size=5000, overlap=500, k=1). Which changes might help?<br>
A. Increase k to 5 for more context. &nbsp; B. Decrease chunk_size to 500 for more focused chunks. &nbsp; C. Remove chunk_overlap completely.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q7 (SA).</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
<pre style="background:#f5f5f5;padding:8px;">text = "Hello world. How are you? I am fine."
splitter = RecursiveCharacterTextSplitter(chunk_size=15, chunk_overlap=5)
print(len(splitter.split_text(text)))</pre>
Output? — <i>Possible answer: 3</i>
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 7</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → B (RAG).</b> Answering strictly from internal documents with minimal hallucination is exactly RAG's job. Temperature/top-p/top-k only tune sampling; fine-tuning bakes knowledge in but doesn't guarantee grounding on specific documents.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → B.</b> RAG looks information up at query time (Googling); fine-tuning stores it in the weights (learning permanently).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → B.</b> The supported way to cap results is <code>as_retriever(search_kwargs={"k": 2})</code>. <code>retriever.k=2</code> and <code>as_retriever(k=2)</code> don't set the search k.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → D (increase k).</b> Multi-document synthesis needs more chunks in context; raising k retrieves more relevant chunks to combine. Changing chunk_size/overlap alters chunk shape but doesn't directly bring in more documents.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → A.</b> <code>similarity_search</code> returns a list of <code>Document</code> objects, so <code>results[0]</code> is a <code>Document</code>.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → A and B.</b> More context (k=5) and smaller, more focused chunks (500) both help relevance. Removing overlap tends to lose boundary context and usually hurts, so C is not selected.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q7 → 3.</b> With chunk_size=15 and overlap=5, the recursive splitter breaks the 36-character text into <b>3</b> chunks (it splits on separators/spaces so pieces stay ≤ ~15 chars while overlapping 5). ✅
</div>

---
<h1 id="week8" style="color:#fff; background:#4527a0; padding:16px; border-radius:12px;">🟣 WEEK 8 — Agents &amp; Autonomous AI (LangChain, LangGraph)</h1>

<p style="color:#555;"><b>Topics:</b> AI agents · the agent loop · tool use &amp; planning · agent frameworks · LangGraph (nodes, edges, state, graphs) · building a multi-step agent</p>

<h2 style="color:#4527a0;">📖 NOTES</h2>

<h3 style="color:#311b92;">1. What is an AI Agent?</h3>
An <b>AI agent</b> is a system that can <b>perceive, reason, and act autonomously</b> to achieve goals. It goes beyond a plain chatbot: it can <b>plan, use tools, remember context, and adapt</b>.
<br><i>Example:</i> an email assistant that reads, summarizes, drafts, and learns user preferences.

<h3 style="color:#311b92;">2. The Core Agent Cycle — Think → Act → Observe (→ Learn)</h3>
<table style="border-collapse:collapse;">
<tr style="background:#ede7f6;"><th style="padding:6px;border:1px solid #b39ddb;">Phase</th><th style="padding:6px;border:1px solid #b39ddb;">What happens</th></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>Think</b></td><td style="padding:6px;border:1px solid #b39ddb;">Decide the next action based on current context.</td></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>Act</b></td><td style="padding:6px;border:1px solid #b39ddb;">Perform actions (tool call, data fetch, send a message).</td></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>Observe</b></td><td style="padding:6px;border:1px solid #b39ddb;">Capture results and update internal state.</td></tr>
</table>
This forms a <b>continuous feedback loop</b> that enables autonomy.

<h3 style="color:#311b92;">3. Key components of an agent</h3>
<ul>
<li><b>Reasoning</b> — decides what to do next.</li>
<li><b>Memory</b> — remembers past interactions and context.</li>
<li><b>Tools</b> — APIs, search engines, calculators, etc.</li>
<li><b>Environment</b> — the system or data the agent interacts with.</li>
</ul>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>Why not just an LLM?</b> LLMs alone only generate text from a prompt — no planning, no persistence, can't autonomously use multiple tools or keep long-term memory. Agents add <b>structure, logic and state management</b> on top of an LLM.
</div>

<h3 style="color:#311b92;">4. Agent frameworks compared</h3>
<table style="border-collapse:collapse;">
<tr style="background:#ede7f6;"><th style="padding:6px;border:1px solid #b39ddb;">Framework</th><th style="padding:6px;border:1px solid #b39ddb;">Focus / strength</th><th style="padding:6px;border:1px solid #b39ddb;">Best for</th></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>LangChain</b></td><td style="padding:6px;border:1px solid #b39ddb;">Prompt chaining, tool calls, simple memory</td><td style="padding:6px;border:1px solid #b39ddb;">Simple, single-agent tasks</td></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>CrewAI</b></td><td style="padding:6px;border:1px solid #b39ddb;">Multi-agent collaboration, task delegation</td><td style="padding:6px;border:1px solid #b39ddb;">Teams of specialized agents</td></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>AutoGen</b> (Microsoft)</td><td style="padding:6px;border:1px solid #b39ddb;">Advanced conversational/research agents, memory</td><td style="padding:6px;border:1px solid #b39ddb;">Experimental research (more setup)</td></tr>
<tr><td style="padding:6px;border:1px solid #b39ddb;"><b>LlamaIndex</b></td><td style="padding:6px;border:1px solid #b39ddb;">RAG / indexing over documents</td><td style="padding:6px;border:1px solid #b39ddb;">Document-heavy retrieval tasks</td></tr>
<tr style="background:#f3e5f5;"><td style="padding:6px;border:1px solid #b39ddb;"><b>LangGraph</b></td><td style="padding:6px;border:1px solid #b39ddb;">Graph-based: nodes, edges, conditional branching, memory, multi-agent</td><td style="padding:6px;border:1px solid #b39ddb;">Deterministic, interpretable, structured workflows</td></tr>
</table>

<h3 style="color:#311b92;">5. LangGraph fundamentals</h3>
<b>Node</b> = a task/action (an LLM reasoning step, a tool call, a memory update). <b>Edge</b> = a connection defining flow of execution; edges can be <b>conditional</b> (branching &amp; loops). <b>State</b> = a shared object carrying all data between nodes.
<div style="background:#e8f5e9;border-left:5px solid #2e7d32;padding:10px;">
<b>🧠 Role of State (tested):</b> State acts as <b>shared memory that passes data between nodes</b> and <b>stores intermediate results</b> produced by each node. It does <b>NOT</b> define execution order (edges do) and is <b>NOT</b> auto-reset after each node.
</div>

<b>Building &amp; running a graph — canonical API</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langgraph.graph import StateGraph, START, END
from typing import TypedDict

class State(TypedDict):        # the schema the graph passes around
    messages: list

builder = StateGraph(State)
builder.add_node("agent", agent_fn)      # register a node: name + callable
builder.add_node("tool",  tool_fn)

builder.set_entry_point("agent")         # where execution begins
# (equivalently: builder.add_edge(START, "agent"))

builder.add_edge("agent", "tool")        # unconditional edge
builder.add_edge("tool", END)            # finish

app = builder.compile()                  # COMPILE the graph -> runnable
result = app.invoke({"messages": []})    # RUN it
</pre>

<b>Conditional routing</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
graph.add_conditional_edges(
    "agent",                                   # source node
    lambda state: "tool" if state["tool_call"] else END   # routing function
)
# or with an explicit mapping (as in the email assistant):
graph.add_conditional_edges("spam_filter", route_after_spam_check,
    {"handle_spam": "handle_spam", "categorize_emails": "categorize_emails"})
</pre>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Key method distinctions:</b><br>
• <code>add_edge(a, b)</code> — always go a→b (unconditional).<br>
• <code>add_conditional_edges(src, fn)</code> — branch based on a function of state (this is how "if tool call → tool, else END" is done).<br>
• <code>set_entry_point("x")</code> — set the start node. <code>set_finish_point("x")</code> — mark an end. There is <b>no</b> conditional behaviour in <code>add_edge</code>.
</div>

<b>Compile / run vocabulary</b>
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
app = graph.compile()      # build -> runnable       (NOT connect()/setup()/run())
out = app.invoke(input)    # execute                 (NOT execute()/call()/output())
</pre>

<h3 style="color:#311b92;">6. State schema &amp; entry-point pitfalls</h3>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Node output must match the state schema.</b> If a node returns <code>{"output": ...}</code> but the schema only declares <code>messages: list</code>, and the graph expects <code>state["input"]</code>/messages keys that were never set, you get a <b>runtime error due to a missing state key</b> — the LLM does not magically convert inputs to messages.
</div>
<div style="background:#fff3e0;border-left:5px solid #ef6c00;padding:10px;">
<b>⚠️ Missing entry point.</b> If you add nodes but never call <code>set_entry_point()</code> / <code>add_edge(START, ...)</code>, then <code>graph.invoke()</code> <b>raises a runtime error</b> — the graph doesn't know where to start; it does not silently run "agent" or return empty state.
</div>

<h3 style="color:#311b92;">7. Node return values &amp; state merging</h3>
A node returns a partial-state dict that is <b>merged</b> into the state. For the greeting graph:
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
class SimpleState(TypedDict):
    name: str
    message: str
graph.add_node("greet", lambda x: {"message": f"Hello {x['name']}!"})
graph.set_entry_point("greet")
graph.add_edge("greet", END)
app = graph.compile()
app.invoke({"name": "Sachin"})
# -> {"name": "Sachin", "message": "Hello Sachin!"}
</pre>
The input <code>name</code> stays in state and the node adds <code>message</code>, so the final state has <b>both keys</b>.

<h3 style="color:#311b92;">8. Worked example — the Intelligent Email Assistant (from the notebook)</h3>
Workflow: <code>read_emails → spam_filter → (conditional) → categorize → summarize → draft → review → send / handle_spam → END</code>.
<pre style="background:#0d1b2a;color:#e0e0e0;padding:12px;border-radius:8px;">
from langgraph.graph import StateGraph, START, END
from langchain_groq import ChatGroq
from typing import List, TypedDict

llm = ChatGroq(model="openai/gpt-oss-20b", temperature=0)

class EmailState(TypedDict):
    emails: List[str]; spam_flags: List[str]; categories: List[str]
    summaries: List[str]; replies: List[str]; reviewed_replies: List[str]

graph = StateGraph(EmailState)
graph.add_node("read_emails", read_emails)
graph.add_node("spam_filter", spam_filter_node)
# ... more nodes ...
graph.add_edge(START, "read_emails")
graph.add_edge("read_emails", "spam_filter")
graph.add_conditional_edges("spam_filter", route_after_spam_check,
    {"handle_spam": "handle_spam", "categorize_emails": "categorize_emails"})
compiled_graph = graph.compile()
final_state = compiled_graph.invoke({"emails": sample_emails})
</pre>
Visualize with <code>display(Image(compiled_graph.get_graph().draw_mermaid_png()))</code>.

<h2 style="color:#6a1b9a;">❓ QUESTIONS — Week 8</h2>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q1.</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span><br>
Fill the missing calls: <code>app = graph.____();  output = app.____({"query":"What is LangGraph?"})</code><br>
A. connect(), execute() &nbsp; B. run(), output() &nbsp; C. setup(), call() &nbsp; D. compile(), invoke()
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q2 (MSQ).</b> <span style="background:#c62828;color:#fff;padding:2px 8px;border-radius:10px;">🔥 VERY HIGH</span><br>
In LangGraph, which statements correctly describe the role of <b>State</b>? (select all)<br>
A. State acts as shared memory that passes data between nodes.<br>
B. State defines the execution order of nodes in the graph.<br>
C. State is automatically reset after every node execution.<br>
D. State stores intermediate results produced by each node during execution.
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q3.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Agent: start at agent node; if LLM response contains a tool call go to tool, else end. Which line adds conditional routing?<br>
A. <code>workflow.add_edge("agent", "tool")</code><br>
B. <code>workflow.add_edge("agent", END)</code><br>
C. <code>workflow.add_conditional_edges("agent", lambda state: "tool" if state["tool_call"] else END)</code><br>
D. <code>workflow.set_finish_point("agent")</code>
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q4.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
Greeting workflow: fill <code>graph.set_entry_point(__)</code> and <code>graph.add_edge("greet", __)</code>.<br>
A. "END", "greet" &nbsp; B. "greet", END &nbsp; C. "start", "end" &nbsp; D. "entry", "exit"
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q5.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
SimpleState has name &amp; message; node greet returns <code>{"message": f"Hello {x['name']}!"}</code>; entry=greet, edge greet→END. Output of <code>app.invoke({"name": "Sachin"})</code>?<br>
A. <code>{"message": "Hello Sachin!"}</code> &nbsp; B. <code>{"Hello Sachin!"}</code> &nbsp; C. <code>{"name": "Sachin", "message": "Hello Sachin!"}</code> &nbsp; D. None
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q6.</b> <span style="background:#2e7d32;color:#fff;padding:2px 8px;border-radius:10px;">✔️ MEDIUM</span><br>
A node writes <code>{"output": response}</code> but the state schema is <code>class State(TypedDict): messages: list</code> (and the node reads <code>state["input"]</code>). Most likely result?<br>
A. LLM auto converts input to messages &nbsp; B. Runtime error due to missing state key &nbsp; C. Graph ignores output &nbsp; D. Messages auto populated
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q7.</b> <span style="background:#ef6c00;color:#fff;padding:2px 8px;border-radius:10px;">⭐ HIGH</span><br>
ReAct-style agent adds nodes "agent" and "tool" then <code>graph = builder.compile()</code> — but no entry point / edges are set. What happens on <code>graph.invoke()</code>?<br>
A. Executes the agent node and returns updated state &nbsp; B. Executes the tool node directly &nbsp; C. Raises a runtime error due to missing entry point &nbsp; D. Returns an empty state without executing any node
</div>

<div style="border:1px solid #ce93d8;border-radius:8px;padding:12px;margin-bottom:10px;">
<b>Q8.</b> <span style="background:#546e7a;color:#fff;padding:2px 8px;border-radius:10px;">• STANDARD</span> <i>(agent concepts, from slides)</i><br>
Which are the four key components of an AI agent? Reasoning, Memory, Tools, and ____?<br>
A. Environment &nbsp; B. Database &nbsp; C. Compiler &nbsp; D. Scheduler
</div>

<h2 style="color:#2e7d32;">✅ SOLUTIONS — Week 8</h2>

<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q1 → D. compile(), invoke().</b> You <code>compile()</code> a StateGraph into a runnable, then <code>invoke()</code> it with the input dict.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q2 → A and D.</b> State is shared memory carrying data between nodes and holding intermediate results. Execution order is defined by edges (B false); state isn't auto-reset per node (C false).
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q3 → C.</b> Branching on the LLM output requires <code>add_conditional_edges</code> with a routing function. Plain <code>add_edge</code> is unconditional; <code>set_finish_point</code> just marks an end.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q4 → B. "greet", END.</b> Entry point is the "greet" node (a string name); the edge goes from "greet" to the special <code>END</code> sentinel.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q5 → C.</b> The input key <code>name</code> stays in state; the node merges in <code>message</code>. Final state has both → <code>{"name": "Sachin", "message": "Hello Sachin!"}</code>.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q6 → B.</b> Reading a key that was never placed in state (and returning a key outside the schema) leads to a runtime error over the missing state key. Nothing is auto-converted.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q7 → C.</b> With no entry point/edges, the graph has no starting node, so <code>invoke()</code> raises a runtime error.
</div>
<div style="border-left:5px solid #2e7d32;padding:10px;background:#f1f8e9;margin-bottom:10px;">
<b>Q8 → A. Environment.</b> The four components are Reasoning, Memory, Tools, Environment.
</div>

---

<h2 id="cheatsheet" style="color:#4527a0;">🎓 FINAL EXAM-DAY CHEAT SHEET</h2>
<table style="border-collapse:collapse; width:100%;">
<tr style="background:#4527a0; color:#fff;"><th style="padding:8px;">Idea</th><th style="padding:8px;">One-liner</th></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">NumPy axis</td><td style="padding:8px;">axis=0 → down columns (per-column); axis=1 → across rows (per-row).</td></tr>
<tr><td style="padding:8px;">pd.merge how</td><td style="padding:8px;">inner=both, left=all left, outer=union, cross=cartesian.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">pivot</td><td style="padding:8px;">long→wide: index=, columns=, values=.</td></tr>
<tr><td style="padding:8px;">Training loop</td><td style="padding:8px;">zero_grad → forward → loss → backward → step.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">No-grad eval</td><td style="padding:8px;">torch.no_grad() / requires_grad=False stop tracking; model.eval() only changes layer behaviour.</td></tr>
<tr><td style="padding:8px;">Dataset overrides</td><td style="padding:8px;">__getitem__ &amp; __len__.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">.to('cuda')</td><td style="padding:8px;">move tensor to GPU.</td></tr>
<tr><td style="padding:8px;">Image shapes</td><td style="padding:8px;">gray (H,W) 0–255; RGB (H,W,3); PIL=RGB, cv2=BGR.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">NMS</td><td style="padding:8px;">keep highest-confidence box, suppress high-overlap rivals.</td></tr>
<tr><td style="padding:8px;">Tokenizer</td><td style="padding:8px;">padding+truncation+max_length → all seqs equal length; special tokens still added.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">Temperature</td><td style="padding:8px;">0 = deterministic; higher = more random.</td></tr>
<tr><td style="padding:8px;">batch()</td><td style="padding:8px;">list in → list of response objects out, same order.</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">RAG vs FT</td><td style="padding:8px;">RAG=Google now; Fine-tune=learn permanently.</td></tr>
<tr><td style="padding:8px;">Retriever k</td><td style="padding:8px;">as_retriever(search_kwargs={"k": n}).</td></tr>
<tr style="background:#f4f0ff;"><td style="padding:8px;">LangGraph run</td><td style="padding:8px;">compile() then invoke(); branch with add_conditional_edges; set_entry_point required.</td></tr>
</table>

<p align="center" style="color:#4527a0; font-size:15px; margin-top:16px;"><b>Good luck! 🍀 Revise the cheat sheet last, and re-do every SOLUTIONS block from memory.</b></p>
