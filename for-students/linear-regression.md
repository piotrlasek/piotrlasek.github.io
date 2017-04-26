import pandas as pd
from sklearn.linear_model import LinearRegression

data = pd.read_csv('../data/data.csv')
df = pd.DataFrame(data)
X_t = df[['s']]
y_t = df['v']
pred_model = LinearRegression()
pred_model.fit(X_t, y_t)
pred_model.predict([3])
