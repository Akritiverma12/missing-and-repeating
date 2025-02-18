# missing-and-repeating
vector<int> findTwoElement(vector<int>& arr) {
        // code here
        long long n=arr.size();
        long long s1=(n*(n+1))/2;
        long long s2=(n*(n+1)*((2*n)+1))/6;
        long long s11=0,s21=0;
        for(long long i=0;i<n;i++){
            s11=s11+arr[i];
            s21=s21+((long long)arr[i]*(long long)arr[i]);
        }
        long long a=s11-s1;
        long long b=s21-s2;
        long long re,mi;
       
        re=(a+(b/a))/2;
        mi=((b/a)-a)/2;
        return {re,mi};
    }
