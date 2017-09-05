# sumExperience
总结开发过程遇到的坑、学习到的技术点

1，下拉分页加载

 效果图：![paginationImg](https://github.com/ruynzhang/sumExperience/tree/master/readMeImg/pagination1.png)
 ![paginationImg2](https://github.com/ruynzhang/sumExperience/tree/master/readMeImg/pagination2.png)
 
 使用mint-ui的InfiniteScroll,Spinner分页加载
 
 主要的实现代码：
        /**
           * 到底自动加载数据
           */
          loadListData() {
              this.pageIndex++;
              this.loading = true;
              this.timerOut =setTimeout(() => {
               this.getListData();
              },1000);
          },
          /**总条数**/
          getListPage(totalCount){
              let totalPage = Math.ceil(totalCount / this.pageSize);//总页数
              if((parseInt(this.pageIndex)+1) >= totalPage){
                this.pageIndex = totalPage;
              }
              this.isLastPage = totalPage == this.pageIndex ? true : false;
              this.loading = this.isLastPage == true ? true : false;
           }
 

2，菜单左右滑动

3，城市选择器

4，手机区号选择器
