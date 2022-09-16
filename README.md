# cyclicsort
# write cyclic sort program in java.
package vishal;

import java.util.Arrays;

public class cyclicsort {
	public static void main(String[] args) {
		int[] arr = {1,4,3,2};
		sort(arr);
		System.out.println(Arrays.toString(arr));
	//	int no = missingnumber(arr);
		//System.out.println(no);
	}
  
	//this sorting program only works when the elements int the array are 1 till n
	//and continuous
  
	static void sort(int[] nums) {
		int i=0;
		while(i<nums.length) {
			int correct = nums[i]-1;  //the correct index of element in 1 till n array is number - 1
			 if(nums[i]==nums.length) {
					i++;
				}
			else if(nums[i] != nums[correct]) {  // checking if the number is right position till it place on rigth index
				swap(nums,i,correct);
			}
			
			else {   // if it place on right index then only it increament the i
				i++;
			}
		}
	}
	static void swap(int[] nums, int first, int second) {
		int temp = nums[first];      // this function is used to wap the numbers.
		nums[first]=nums[second];
		nums[second]=temp;
	}
	/*static int missingnumber(int[] nums) {
		for(int i=1; i<nums.length; i++){
            if(nums[i]!=i){
                return i;
            }
        }
        return nums.length;
	}*/
	
}
