class Solution {
    public int threeSumMulti(int[] arr, int target) {
        int mod = 1_000_000_007;
        long result = 0;
        for(int i = 0; i < arr.length; i++){
            int count[] = new int[101];
            for(int j = i+1; j < arr.length; j++) {
                int k = target - arr[i] - arr[j];
                if(k>=0 && k<=100 && count[k]>0){
                    result+=count[k];
                    result%=mod;
                }
                count[arr[j]]++;
            }
        }
        return (int)result;
    }
}

class Solution {
    public int threeSumMulti(int[] arr, int target) {
        int mod = 1_000_000_007;
        long result = 0; 
        long[] c = new long[101];
        for(int i : arr) c[i]++;
        
        for(int i = 0; i <= 100; i++) {
            for(int j = i; j <= 100; j++) {
                int k = target-i-j;
                if(k<0 || k >100) continue;
                if(i == j && j==k) {
                    result+= (c[i] * (c[i]-1) * (c[i]-2) /6);
                }
                else if(i == j && j != k) {
                    result += ((c[i] * (c[i]-1) /2 ) * c[k]);
                }
                else if(i < j && j < k) {
                    result += (c[i] * c[j] * c[k]);
                }
            }
        }
        return (int)(result%mod);
    }
}
