class Solution {
    public List<Double> averageOfLevels(TreeNode root) {
        List<Double> result = new ArrayList<>();
        Queue<TreeNode> q = new LinkedList<>();
        q.add(root);
        while(!q.isEmpty()) {
            int size = q.size();
            long sum = 0;
            for(int i = 0; i < size; i++) {
                TreeNode curr = q.poll();
                sum+=curr.val;
                if(curr.left != null) q.add(curr.left);
                if(curr.right != null) q.add(curr.right);
            }
            result.add((double)sum/size);
        }
        return result;
    }
}
