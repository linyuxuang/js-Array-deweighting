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



         不给予原型链写字符串去重？？怎么做了，看下面
         
         
             var  arr="aaassshhh"
                //console.log(arr.split(""))
                var split_arr=arr.split("")
                for(var i=0;i<split_arr.length;i++){
                  for(var j=0;j<split_arr.length;j++){
                        if(split_arr[i]==split_arr[j]){
                             split_arr.splice(j,1); 		
                        }
                  }

                }

                 console.log(split_arr)    //["a", "s", "h"]
                 
   数组获取相同元素
    
       var arr=["1111",'222222','222222','222222',"1111","1111","333333","333333"]
         function refrain(arr) {
          var tmp = [];
          if(Array.isArray(arr)) {
        　　  arr.concat().sort().sort(function(a,b) {
          　if(a==b && tmp.indexOf(a) === -1){
              tmp.push(a);
           }
          });
         }
        return tmp;
       }
     
      
        var testArr=[]
         for (let i=0;i<arr.length;i++) {
          for (let j=i;j<arr.length;j++) {
           if(arr[i]==arr[j]&&testArr.indexOf(arr[i])===-1) {
            testArr.push(arr[i])
           }
         }     
      }

   
             
   
   
   
   
   
                 
       
  
  










