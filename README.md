# zokrates-toy-ex
### Toy example of zoKrates

in ``src``, you can find 3 directories: 
- ```dont_work_and_shouldnt``` in this dir we can find code that don't pass the proof, but should not.
- ```work_but_shouldnt``` in this dir we can find code that pass the proof, but should not.
- ```work_but_should``` in this dir we can find code that pass the proof, and should.

in ```dont_work_and_shouldnt```:
- in ```Struct```, alice and bob return a struct that has one parameter that differs: it should not pass the proof. 
- in ```Struct_diff_input```, alice and bob return a struct that has one parameter that differs but have different inputs so that the difference of the inputs should yield the same value for the struct. However, the code is different: it should not pass the proof. 

in ```work_and_should```:
- in ``add``, alice and bob return the addition of two inputs, the codes are similar, inputs are the same: it should pass the proof.
- in ``add_diff_input``, alice and bob return the addition of two inputs, the codes are similar but the inputs are different: it should pass the proof.

in ```work_and_shouldnt```:
- in ``add_hardcoded``, alice returns the addition of two inputs while bob returns hardcoded value of 4. And the inputs of Alice is 2+2: it should not pass the proof yet it does.
- in ``Struct``, alice returns a parameter of a struct while bob returns hardcoded value. However, the inputs make the value of the result of Bob and Alice to be similar: it should not pass the proof yet it does.
