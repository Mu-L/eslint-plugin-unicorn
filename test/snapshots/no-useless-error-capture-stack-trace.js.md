# Snapshot report for `test/no-useless-error-capture-stack-trace.js`

The actual snapshot is saved in `no-useless-error-capture-stack-trace.js.snap`.

Generated by [AVA](https://avajs.dev).

## invalid(1): class MyError extends Error { constructor() { Error.captureStackTrace(this, MyError); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError);␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(2): class MyError extends Error { constructor() { Error.captureStackTrace?.(this, MyError); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace?.(this, MyError);␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace?.(this, MyError);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(3): class MyError extends Error { constructor() { Error.captureStackTrace(this, this.constructor); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, this.constructor);␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, this.constructor);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(4): class MyError extends Error { constructor() { Error.captureStackTrace(this, this.constructor); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, this.constructor);␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, this.constructor);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(5): class MyError extends Error { constructor() { Error.captureStackTrace?.(this, this.constructor); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace?.(this, this.constructor);␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace?.(this, this.constructor);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(6): class MyError extends Error { constructor() { Error.captureStackTrace(this, new.target); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, new.target);␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, new.target);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(7): class MyError extends Error { constructor() { Error.captureStackTrace?.(this, new.target); } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace?.(this, new.target);␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace?.(this, new.target);␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(8): class MyError extends Error { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(9): class MyError extends EvalError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends EvalError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends EvalError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends EvalError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(10): class MyError extends RangeError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends RangeError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends RangeError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends RangeError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(11): class MyError extends ReferenceError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends ReferenceError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends ReferenceError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends ReferenceError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(12): class MyError extends SyntaxError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends SyntaxError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends SyntaxError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends SyntaxError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(13): class MyError extends TypeError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends TypeError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends TypeError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends TypeError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(14): class MyError extends URIError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends URIError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends URIError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends URIError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(15): class MyError extends AggregateError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends AggregateError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends AggregateError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends AggregateError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(16): class MyError extends SuppressedError { constructor() { Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends SuppressedError {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | class MyError extends SuppressedError {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends SuppressedError {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, MyError)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(17): class MyError extends Error { constructor() { const foo = () => { Error.captureStackTrace(this, MyError) } } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		const foo = () => {␊
      4 | 			Error.captureStackTrace(this, MyError)␊
      5 | 		}␊
      6 | 	}␊
      7 | }␊
    `

> Output

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		const foo = () => {␊
      4 | 			␊
      5 | 		}␊
      6 | 	}␊
      7 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		const foo = () => {␊
    > 4 | 			Error.captureStackTrace(this, MyError)␊
        | 			^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      5 | 		}␊
      6 | 	}␊
      7 | }␊
    `

## invalid(18): class MyError extends Error { constructor() { if (a) Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		if (a) Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		if (a) Error.captureStackTrace(this, MyError)␊
        | 		       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(19): class MyError extends Error { constructor() { const x = () => Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		const x = () => Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		const x = () => Error.captureStackTrace(this, MyError)␊
        | 		                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(20): class MyError extends Error { constructor() { void Error.captureStackTrace(this, MyError) } }

> Input

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
      3 | 		void Error.captureStackTrace(this, MyError)␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | class MyError extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		void Error.captureStackTrace(this, MyError)␊
        | 		     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(21): export default class extends Error { constructor() { Error.captureStackTrace(this, new.target) } }

> Input

    `␊
      1 | export default class extends Error {␊
      2 | 	constructor() {␊
      3 | 		Error.captureStackTrace(this, new.target)␊
      4 | 	}␊
      5 | }␊
    `

> Output

    `␊
      1 | export default class extends Error {␊
      2 | 	constructor() {␊
      3 | 		␊
      4 | 	}␊
      5 | }␊
    `

> Error 1/1

    `␊
      1 | export default class extends Error {␊
      2 | 	constructor() {␊
    > 3 | 		Error.captureStackTrace(this, new.target)␊
        | 		^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      4 | 	}␊
      5 | }␊
    `

## invalid(22): export default ( class extends Error { constructor() { Error.captureStackTrace(this, new.target) } } )

> Input

    `␊
      1 | export default (␊
      2 | 	class extends Error {␊
      3 | 		constructor() {␊
      4 | 			Error.captureStackTrace(this, new.target)␊
      5 | 		}␊
      6 | 	}␊
      7 | )␊
    `

> Output

    `␊
      1 | export default (␊
      2 | 	class extends Error {␊
      3 | 		constructor() {␊
      4 | 			␊
      5 | 		}␊
      6 | 	}␊
      7 | )␊
    `

> Error 1/1

    `␊
      1 | export default (␊
      2 | 	class extends Error {␊
      3 | 		constructor() {␊
    > 4 | 			Error.captureStackTrace(this, new.target)␊
        | 			^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ Unnecessary \`Error.captureStackTrace(…)\` call.␊
      5 | 		}␊
      6 | 	}␊
      7 | )␊
    `
