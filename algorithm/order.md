#### 快速排序

- 时间复杂度

  最坏情况下O(n^2),最好情况下O(nlogn)

- 空间复杂度

  O(logn)

```java
public void quickSoft(int[] nums, int l, int r) {
    if (l < r) {
        int i = l;
        int j = r;
        int x = nums[i];
        while (i < j) {
            while (i < j && nums[j] >= x) {
                j--;
                }
                if (i < j) {
                    nums[i++] = nums[j];
                }
                while (i < j && nums[i] <= x) {
                i++;
                }
                if (i < j) {
                    nums[j++] = nums[i];
                }
            }
            nums[i] = x;
        quickSoft(nums, l, i - 1);
        quickSoft(nums, i + 1, r);
    }
}
```

#### 冒泡排序

- 时间复杂度

  O(n^2)

- 空间复杂度

  O(1)

```java
public void bubbleSoft(int[] nums) {
    for (int a = 0;a < nums.length - 1;a++) {
        for (int b = 0;b < nums.length - 1 - a;b++) {
            if (nums[b] > nums[b + 1]) {
                int temp = nums[b];
                nums[b] = nums[b + 1];
                nums[b + 1] = temp;
            }
        }
    }
}
```

#### 选择排序

- 时间复杂度

  O(n^2)

- 空间复杂度

  O(1)

```java
public void selectSoft(int[] nums) {
    for (int a = 0;a < nums.length - 1;a++) {
        for (int b = a + 1;b < nums.length;b++) {
            if (nums[a] > nums[b]) {
                int temp = nums[b];
                nums[b] = nums[a];
                nums[a] = temp;
            }
        }
    }
}
```
