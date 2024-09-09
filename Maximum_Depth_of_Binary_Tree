/** 104. Maximum Depth of Binary Tree
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
public class Maximum_Depth_of_Binary_Tree {
    public int maxDepth(TreeNode root) {
        if (root==null) return 0;
        return treedepthFinder(root,1,1);
    }
    public int treedepthFinder(TreeNode newRoot,int maxDepth, int curDepth){
        boolean hasSibling=false;
        if(newRoot.left!=null){
            hasSibling=true;
            curDepth+=1;
            maxDepth=treedepthFinder(newRoot.left,maxDepth,curDepth);
        }
        if(newRoot.right!=null){
            if(!hasSibling) curDepth++;
           maxDepth= treedepthFinder(newRoot.right,maxDepth,curDepth);
        }
        if(curDepth>maxDepth) return curDepth;
        return maxDepth;
    }
}
