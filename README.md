# JMeter
## JMeter via GUI <br>
- ### test_plan_2
<img width="700" alt="Screen Shot 2024-03-13 at 13 15 33" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/36f75c6f-9d12-4ba5-bac5-d199360e4871"> <br>
- ### test_plan_3
<img width="700" alt="Screen Shot 2024-03-13 at 13 19 12" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/e985c7aa-245a-4df9-8232-bdf5a438b827"> <br>

## JMeter via Command Line/Terminal
- ### test_plan_2
<img width="685" alt="Screen Shot 2024-03-13 at 13 32 15" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/629bcae2-7935-4e82-9165-e2cf4d3804d8"> <br>
- ### test_plan_3
<img width="684" alt="Screen Shot 2024-03-13 at 13 32 47" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/ef910cc7-3e27-4afc-bbc6-2b8a58b52a06"> <br>
<br>
# Optimization Proof
- ## test_plan_1
  ### Before
  <img width="700" alt="Screen Shot 2024-03-13 at 16 17 23" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/6da5c6e0-10d2-47fb-b750-79adbe57c53d"> <br>
  ### After
  <img width="700" alt="Screen Shot 2024-03-13 at 16 11 49" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/948c41e8-e31a-4c4d-acc9-801d49a13aad"> <br>
- ## test_plan_2
  ### Before
  <img width="700" alt="Screen Shot 2024-03-13 at 13 15 33" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/36f75c6f-9d12-4ba5-bac5-d199360e4871"> <br>
  ### After
  <img width="700" alt="Screen Shot 2024-03-13 at 16 28 11" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/a2150564-d2a1-499e-bf10-6a7b2ecb591f"> <br>
- ## test_plan_3
  ### Before
  <img width="700" alt="Screen Shot 2024-03-13 at 13 19 12" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/e985c7aa-245a-4df9-8232-bdf5a438b827"> <br>
  ### After
  <img width="700" alt="Screen Shot 2024-03-13 at 16 23 46" src="https://github.com/farrelayman09/exercise-profiling/assets/125422538/1ebd4d4b-7209-4293-8f31-ef9ff94d0dfa">
<br>

## Explanation
From the comparison images above it is visible that a lot of changes occured. These are the details of time execution ranges comparison before and after optimization (in ms):<br>

**test_plan_1**<br>
Before: 52307-55380<br>
After: 3324-3787<br>

**test_plan_2**<br>
Before: 1409-1932<br>
After: 64-251<br>

**test_plan_3**<br>
Before: 65-148<br>
After: 56-99<br>

From the comparison images above it is visible that before optimization occured, the execution time is relatively long. But, after optimization, all the execution time has been reduced which will in turn enhance the performance of the code. 

# Reflection
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance? <br>
JMeter is primarily used for load and stress testing applications to evaluate how well they perform under conditions such as heavy user loads, concurrent requests, etc. It helps in identifying bottlenecks and weaknesses in the application's architecture, infrastructure, or codebase. Meanwhile, Profiling with IntelliJ Profiler is used to analyze the runtime behavior of an application, focusing on the usage of CPU, memory allocation, thread activity, method execution times, etc. It helps in identifying areas of the code that are consuming the most resources and causing performance bottlenecks.

2. How does the profiling process help you in identifying and understanding the weak points in your application?<br>
Profiling helps me by providing me crucial evaluation points in the form of Flame graph, Call tree, Method list, Timeline, and Events. Within these visuals, there are also important information in the form of percentages of CPU times and method execution length. With these items, I gain a better understanding and can bettter optimize my application

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?<br>
I think Intellij has provided a very succinct and informative assessment overall. The profiler generates detailed profiling data such as method execution times, memory allocations, garbage collection activity, etc. This data helps me pinpoint specific areas of the code that may be causing performance bottlenecks or resource inefficiencies.

4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?<br>
At first, I didnt really understand what any of the values meant, especially the way the flame graph works. Therefore, I try to read it carefully while also reading documentation and blogs focusing in the matter.

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?<br>
By using Intellij Profiler, I understand better certain aspects of the code that has relative poor usage of CPU, memory allocation, thread activity, method execution times. This of course will then help me in my code evaluation/optimization process

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?<br>
When the results of, it's essential to consider several factors and approaches to reconcile the differences. Profiler is primarily used to help analyze the intricate details of an application's runtime behavior, tracking various performance metrics such as memory usage, execution speed, thread activity, and more. Meanwhile, JMeter enable it to simulate a heavy load on a server, network, or object to test its strength or analyze overall performance under different load types. Because of this, I think how we analyze the results is mostly based on what type of aspects we want to focus more into (CPU & Performance or server & network load).

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?<br>
One of the strategies I use is to utilize currently-taught materials (in class and in modules) to optimize the application performance. For instance, one of the materials that we were recently taught was StringBuilder. By delving deeper into what StringBuilder is, I now know that StringBuilder outperforms String in Java for performance optimization. String is immutable, whereas StringBuilder is mutable, making it efficient for frequent concatenation, string modification, and large string construction. By using this information, I could then modify such that the method that still uses String object (joinStudentNames) would then use StringBuilder. This will in turn optimize greatly this section of the code. While doing that, I also carefully read and analyze the code changes such that I dont alternate its original functionality.
