# -demo----Array-traversal
前端js中数组遍历的基本6种方式


> **以下的集中循环，除了for循环之外，均含有三个参数**
**1.当前正在遍历的元素**
**2.当前的索引**
**3.当前遍历的数组**
**但是基本常用的就是ele（元素），index（索引）这两个，arr（数组是不太常用的），总而言之想用谁就写谁，ele，index，ele不是固定的，纯属自己个人的喜好**

        //1.
        //****************************for循环*************************************
        //for循环，这个方法大家应该都是会的
        var arr = ['2', '小明', true, 'HelloWorld'];
        for (var i = 0; i < arr.length; i++) {
            console.log(arr[i])
        }

        //2.
        // *******************************forEach******************************
        // forEach遍历数组
        // 循环数组中每一个元素并采取操作，可以不用知道数组长度
        // 返回值：无
        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0, ];
        arr.forEach(function(ele, index) {
            console.log(ele + "-----" + index);
        })

        //3.
        // *******************************some******************************
        // 遍历数组中是否有符合条件的元素
        // 返回值：boolean
        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0, ];
        var result = arr.some(function(ele, i) {
            if (ele > 3) {
                return true;
            }
        })
        console.log(result);

        //4.
        //*****************************fileter*******************************
        //filter遍历数组
        //主要用于筛选
        //返回值 筛选之后的一个新数组
        var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0, ];
        var n = arr.filter(function(ele, index) {
            return ele > 3;
        })
        console.log(n);

        //5.
        //****************************every*************************************
        //every遍历数组
        //遍历数组中是否“每个”元素都符合条件
        //返回Boolean值
        var arr = [1, 3, '小明', true, 'HelloWorld'];
        var newstate = arr.every(function(ele) {
            return typeof ele == 'number'
        })
        console.log(arr, newstate);

        //6.
        //****************************map*************************************
        //map遍历数组
        //遍历数组每个元素，并回调操作，需要返回值
        //返回值组成新的数组，原数组不变
        var arr = ['2', '小明', true, 'HelloWorld'];
        var newstate = arr.map(function(ele) {
            index = "map的" + ele;
            return index;
        })
        console.log("newstate", newstate);
