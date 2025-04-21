#bash #tool #helper #text-processing 

# Convert text to lowercase
```
echo "HAllo 123!!" | tr '[:upper:]' '[:lower:]'
echo "HAllo 123!!" | awk '{print tolower($0)}'
echo "HAllo 123!!" | sed 's/.*/\L&/'
echo "HAllo 123!!" | perl -pe '$_=lc'
```