# js-Array-deweighting
给予原型链分装的数组去重




            var  arr=[1,1,1,1,2,2,2,2,5,6,5,5,4,6,9,0];
              Array.prototype.unique=function(){
                var temp={},
                arr=[],
                len=this.length;
                for(var i=0;i<len;i++){
                  if(temp[i]==undefined){ 也可写成 !temp[i]
                    temp[i]="abc",
                    arr.push(i)
                  }
                }
                 return arr;
              }

            arr.unique() //[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
