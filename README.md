## backend_task_no_deploy


task 1
```python
# Returns true if strA is a subsequence of strB 
# m is length of strA, n is length of strB 
def fun(strA,strB,m,n): 
      
    j = 0    # Index of strA 
    i = 0    # Index of strB 
      
    # Traverse both strA and strB
    # Compare current character of strB with  
    # first unmatched character of strA 
    # If matched, then move ahead in strA
      
    while j<m and i<n: 
        if strA[j] == strB[i]:     
            j = j+1    
        i = i + 1
          
    # If all characters of str1 matched, then j is equal to m 
    return j==m 
      
# Driver Program 
  
strA = "AC"
strB = "ABCD"
m = len(strA) 
n = len(strB) 
  
print "Yes" if fun(strA,strB,m,n) else "No"
```
task 2 
(I didn't understand the problem very well .Here is my solution anyways :/ )
```
URL url = new URL ("https://reqres.in/api/users");
HttpURLConnection con = (HttpURLConnection)url.openConnection();
con.setRequestMethod("POST");
con.setRequestProperty("Content-Type", "application/json; utf-8");
con.setRequestProperty("Accept", "application/json");
con.setDoOutput(true);
String jsonInputString = "{"name": "Upendra", "job": "Programmer"}";
try(OutputStream os = con.getOutputStream()) {
    byte[] input = jsonInputString.getBytes("utf-8");
    os.write(input, 0, input.length);           
}
try(BufferedReader br = new BufferedReader(
  new InputStreamReader(con.getInputStream(), "utf-8"))) {
    StringBuilder response = new StringBuilder();
    String responseLine = null;
    while ((responseLine = br.readLine()) != null) {
        response.append(responseLine.trim());
    }
    System.out.println(response.toString());
}
```

