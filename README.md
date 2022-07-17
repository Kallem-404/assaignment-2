# assaignment-2
df.isnull()      
# Returns a boolean matrix, if the value is NaN then True otherwise False
df.isnull().sum() 
# Returns the column names along with the number of NaN values in that particular column
from sklearn.impute import SimpleImputer
imputer = SimpleImputer(missing_values=np.nan, strategy='mean')
imputer = imputer.fit(df[['Weight']])
df['Weight'] = imputer.transform(df[['Weight']])
from sklearn.preprocessing import StandardScaler
std = StandardScaler()
X = std.fit_transform(df[['Age','Weight']])
df_cat = pd.DataFrame(data = 
                     [['green','M',10.1,'class1'],
                      ['blue','L',20.1,'class2'],
                      ['white','M',30.1,'class1']])
df_cat.columns = ['color','size','price','classlabel']
