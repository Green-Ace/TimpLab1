1) wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz

2) tar -xf boost_1_69_0.tar.gz

3) tree -a -L 1   ![изображение](https://user-images.githubusercontent.com/112771063/223426613-95029c84-f92a-4b9e-94de-37026949e9bb.png)

4) tree -a   ![изображение](https://user-images.githubusercontent.com/112771063/223426783-fee941c8-ba38-40de-aed9-5ecb8620c4f6.png)

5)tree -P *.hpp
  tree -P *.cpp
  62614 - 14914 - 13815 = 77923
  
  6) find $(pwd) -name any.hpp ![изображение](https://user-images.githubusercontent.com/112771063/223428636-b081a497-9046-47c5-a9af-c45d5c8df572.png)


7) grep -r -l "boost::asio" ![изображение](https://user-images.githubusercontent.com/112771063/223428867-250138ba-d616-4db4-9955-b0deb7de91e6.png)


8) cd tools/build
  sh bootstrap.sh      ![изображение](https://user-images.githubusercontent.com/112771063/223430750-2b8104fb-c111-433e-ad34-8d1c8dc20cb2.png)
  ./b2 install --prefix=boost_output
  
  
9) mv boost_output boost-libs

10) cd boost-libs
    find . -type f -exec du -h {} +
   
11) find . -type f -exec du {} +|sort -rh | head -n 10  ![изображение](https://user-images.githubusercontent.com/112771063/223431741-aa589abe-f484-4f4e-b49a-b5be4cf51f5f.png)
