# Iterate over a Vector

    // Iterate over a vector using range based for loop
    for(auto & elem : vec_of_num){
        cout<< elem <<", ";
    }
    
    // Iterate over vector of integers by indexing
    for(int i = 0; i < vec_of_num.size(); i++){
        cout << vec_of_num[i] << " at index position: " << i << endl;
    }
    
    // Iterate over a vector using STL algorithm
    // for_each() and Lambda function
    for_each(vec_of_num.begin(), vec_of_num.end(), [](const auto & elem){
                cout<< elem << ", "; 
        });
        
    // Iterate over a vector of int and get the
    // sum of all itegers in the vector
    int sum = 0;
    for_each(   vec_of_num.begin(), 
                vec_of_num.end(),
                [&sum](const auto & elem){
                    sum = sum + elem;   
                });
                
// Iterate over a vector of integers using iterators
    for(vector<int>::iterator   it = vec_of_num.begin();
                                it != vec_of_num.end();
                                it++ ){
        cout<<*it<<", ";         
    }
  
# Looping through String
  Looping through the characters of a std::string, using a range-based for loop (it's from C++11, already supported in recent releases of GCC, clang, and the VC11 beta):

std::string str = ???;
for(char& c : str) {
    do_things_with(c);
}
Looping through the characters of a std::string with iterators:

std::string str = ???;
for(std::string::iterator it = str.begin(); it != str.end(); ++it) {
    do_things_with(*it);
}
Looping through the characters of a std::string with an old-fashioned for-loop:

std::string str = ???;
for(std::string::size_type i = 0; i < str.size(); ++i) {
    do_things_with(str[i]);
}
Looping through the characters of a null-terminated character array:

char* str = ???;
for(char* it = str; *it; ++it) {
    do_things_with(*it);
}
