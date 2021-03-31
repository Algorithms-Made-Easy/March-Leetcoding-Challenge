class Solution {
    public int[] movesToStamp(String stamp, String target) {
        
        char[] tchar = target.toCharArray();
        char[] schar = stamp.toCharArray();
        int count =0;
        boolean[] visited = new boolean[tchar.length];
        List<Integer> res = new ArrayList<>();
        
        while(count!=tchar.length){
            boolean didchange=false;
            for(int i=0;i<= tchar.length - schar.length;i++){
                if(!visited[i] && canReplace(tchar,i,schar)){
                    count=replace(tchar,i,schar.length,count);
                    visited[i]=true;
                    didchange = true;
                    res.add(i);
                    
                    if(count == tchar.length){
                        break;
                    }
                }
            }
            
            if(!didchange){
                return new int[0];
            }
        }
        
        int[] result = new int[res.size()];
        int k=0;
        for(int i=res.size()-1;i>=0;i--){
            result[k++]=res.get(i);
        }
        
        return result;
    }
    
    boolean canReplace(char[] tchar,int pos, char[] schar){
        for(int i=0;i<schar.length;i++){
            if(tchar[i+pos] != '?' && tchar[i+pos] != schar[i]){
                return false;
            }
        }
        return true;
    }
    
    int replace(char[] tchar, int pos, int len, int count){
        for(int i=0;i<len;i++){
            if(tchar[i+pos] != '?'){
                tchar[i+pos]= '?';
                count++;
            }
        }
        return count;
    }
}
