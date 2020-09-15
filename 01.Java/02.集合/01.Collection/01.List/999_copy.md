# copy

* System.arraycopy() 方法

  ```arraycopy
  int[] a = new int[10];
  a[0] = 0;
  a[1] = 1;
  a[2] = 2;
  a[3] = 3;
  System.arraycopy(a, 2, a, 3, 3);
  //a[2]=99;
  for (int i = 0; i < a.length; i++) {
      System.out.print(a[i]);
  }
  ```

  结果：

  ```结果
  0 1 2 2 3 0 0 0 0 0
  ```

* Arrays.copyOf()方法

  复制一个新的数组
