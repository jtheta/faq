# jtheta.faq

## What is `jtheta`?

`jtheta` is a development platform for building real-world scientific/math-centric applications; primarily for machine / deep learning. It designed to be a foundation for any machine learning team / org.

`jtheta` is focused on practicality, providing more than just math and training implementations. It provides libraries and tools for gathering and cleaning data as well as other common machine learning related tasks.

Here is a brief list of `jtheta`'s features.

 - write `jtheta` functions in matlab / octave and execute them natively in other languages
 - organize, download, and find raw data with `jtheta.gather`
 - use `jtheta.clean` to prepare training data
 - train models with `tensorflow` or implement your own algorithms
 - easily collaborate with mathemiticians
 - re-use existing `matlab` / `octave` code
 - run `jtheta` functions natively in `python`, `node.js`, `java`, `swift`, and in the `browser` with `react` and `angular`!
 - visualize data with hardware accelerated plots and animations (**react / angular only**)

## How much does it cost?

The majority of the `jtheta` platform is open source, with a liberal MIT liscense. The only commercial aspect of the platform is the proprietary hardware and compilers that target that hardware. More info about this coming soon.

## When can I use it?

`jtheta` is currently in early, but open, development. Follow [these repos](http://github.com/jtheta) to stay in the loop.

## How can I write `jtheta` functions?

Below is a simple `jtheta` function, written in octave/matlab syntax.

```matlab
% sigmoid.m
function g = sigmoid(z)
  g = 1.0 ./ (1.0 + exp(-z));
end
```

You can statically compile this function using the `jtheta` compiler.

```sh
jtc sigmoid.m > sigmoid.j
```

`.j` files are execute-able in all languages supported by `jtheta`.

Here is an example calling this sigmoid function, natively in `python`.

```python
import jtheta as jt

def tryJtheta(data):
  return jt('sigmoid', data) # data = 9 => 0.9999
```

You can also, execute `jtheta` functions in modern browsers and other supported JavaScript environments.

```js
// browser (requires webpack)
import jtheta as jt from 'jtheta'

async function tryJTheta(data) {
  await jt('sigmoid', data) // data = 9 => 0.9999
}
```

### To be continued...

**More FAQs to come...** This page is still in the works.





