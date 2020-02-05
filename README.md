{
	"comment": {
		"prefix": "z-comment",
		"body": [
			"/**",
			" * functional react component for ...",
			" * @function",
			" * @param {*} props - props",
			" * @returns {JSX.Element} - react component",
			" */"
		],
		"description": "comment"
	},
	"action thunk": {
		"prefix": "z-redux-thunk-timeout",
		"body": [
			"export const actionName = payload => dispatch => {",
			"  setTimeout(() => {",
			"    dispatch(change(payload))",
			"  }, 400);",
			"}"
		],
		"description": "action thunk"
	},
	"z-redux-actions-rest": {
		"prefix": "z-redux-actions-rest",
		"body": [
			"export const getData = () => dispatch => {",
			"  Axios.get('$1')",
			"    .then(res => {",
			"      if (res.statusText === 'OK') {",
			"        dispatch(first(res)) // first it is action",
			"      }",
			"    })",
			"    .catch(err => dispatch(handleError(err.message)))",
			"      // handleeError it is action",
			"}"
		],
		"description": "z-redux-actions-rest"
	},
	"z-redux-reducer": {
		"prefix": "z-redux-reducer",
		"body": [
			"import { action } from '../actions'",
			"",
			"const initialState = {",
			"",
			"}",
			"",
			"export default (state = initialState, { type, payload }) => {",
			"  switch (type) {",
			"",
			"  case action.$1:",
			"    return { ...state, ...payload }",
			"",
			"  default:",
			"    return state",
			"  }",
			"}"
		],
		"description": "z-redux-reducer"
	},
	"combine reducer": {
		"prefix": "z-redux-combine",
		"body": [
			"import { combineReducers } from 'redux'",
			"",
			"import counter from './counter'",
			"",
			"export default  combineReducers({",
			"  counter",
			"})"
		],
		"description": "combine reducer"
	},
	"z-redux-provider": {
		"prefix": "z-redux-provider",
		"body": [
			"import React from 'react'",
			"import ReactDOM from 'react-dom'",
			"import { Provider } from 'react-redux'",
			"",
			"import App from './App'",
			"import { store } from './store'",
			"",
			"const app = (",
			"  <Provider store={ store }>",
			"    <App />",
			"  </Provider>",
			")",
			"",
			"ReactDOM.render(app, document.getElementById('root'))"
		],
		"description": "z-redux-provider"
	},
	"redux store": {
		"prefix": "z-redux-store",
		"body": [
			"import { createStore, applyMiddleware, compose } from 'redux'",
			"import reduxThunk from 'redux-thunk'",
			"",
			"import rootReducer from './reducers'",
			"",
			"// redux devtools",
			"const composeEnhancers =",
			"  typeof window === 'object' &&",
			"  window.__REDUX_DEVTOOLS_EXTENSION_COMPOSE__ ?   ",
			"    window.__REDUX_DEVTOOLS_EXTENSION_COMPOSE__({",
			"      // Specify extension’s options like name, actionsBlacklist, actionsCreators, serialize...",
			"    }) : compose;",
			"",
			"const enhancer = composeEnhancers(",
			"  applyMiddleware(reduxThunk ),",
			"  // other store enhancers if any",
			");",
			"",
			"",
			"export const store = createStore(",
			"  rootReducer,",
			"  enhancer",
			")"
		],
		"description": "redux store"
	},
	"const destruct": {
		"prefix": "constd",
		"body": [
			"const {  } = "
		],
		"description": "const destruct"
	},
	"zrfcp": {
		"prefix": "z-rfcp",
		"body": [
			"import React from 'react'",
			"import PropTypes from 'prop-types'",
			"",
			"/**",
			" * functional react component for ...",
			" * @function",
			" * @param {*} props - props",
			" * @returns {JSX.Element} - react component",
			" */",
			"function $1({ $2 }) {",
			"  return (",
			"    <div>",
			"      ",
			"    </div>",
			"  )",
			"}",
			"",
			"$1.propTypes = {",
			" ex: PropTypes.func.isRequired",
			"}",
			"",
			"export default $1"
		],
		"description": "zrfcp"
	},
	"zrfc": {
		"prefix": "z-rfc",
		"body": [
			"import React from 'react'",
			"",
			"/**",
			" * functional react component for ...",
			" * @function",
			" * @param {*} props - props",
			" * @returns {JSX.Element} - react component",
			" */",
			"function $1({ $2 }) {",
			"  return (",
			"    <div>",
			"      ",
			"    </div>",
			"  )",
			"}",
			"",
			"export default $1"
		],
		"description": "zrfc"
	},
	"zrfcpr": {
		"prefix": "z-rfcpr",
		"body": [
			"import React from 'react'",
			"import PropTypes from 'prop-types'",
			"import { connect } from 'react-redux'",
			"",
			"/**",
			" * functional react component for ...",
			" * @function",
			" * @param {*} props - props",
			" * @returns {JSX.Element} - react component",
			" */",
			"function $1({ $2 }) {",
			"  return (",
			"    <div>",
			"      ",
			"    </div>",
			"  )",
			"}",
			"",
			"$1.propTypes = {",
			" $2: PropTypes.func.isRequired",
			"}",
			"",
			"const mapStateToProps = state => ({",
			"  ",
			"})",
			"",
			"const mapDispatchToProps = dispatch => ({",
			"  ",
			"})",
			"",
			"export default connect(mapStateToProps, mapDispatchToProps)($1)",
			""
		],
		"description": "zrfcpr"
	},
	"z-test-setupTests": {
		"prefix": "z-test-setupTests",
		"body": [
			"import Enzyme from 'enzyme'",
			"import EnzymeAdapter from 'enzyme-adapter-react-16'",
			"",
			"// comfigure enzyme for all test.js page",
			"// must be in src folder",
			"Enzyme.configure({",
			"    adapter: new EnzymeAdapter(),",
			"    disableLifecycleMethods: true",
			"})"
		],
		"description": "z-setupTests"
	},
	"z-test-utils": {
		"prefix": "z-test-utils",
		"body": [
			"import checkPropTypes from 'check-prop-types'",
			"import { applyMiddleware, createStore } from 'redux'",
			"",
			"import rootReducer from './../src/store/reducers'",
			"import { middlewares } from './../src/store' // must destructurazated midleware!!!",
			"",
			"/**",
			"* find component by data-test",
			"* Return ShallowWrapper containing node(s) with the given data-test",
			"* @param {ShallowWrapper} wrapper - Enzyme shallow wrapper to seacrch",
			"* @param {string} val - Value of data-test attribute for search.",
			"* @returns {ShallowWrapper}",
			"*/",
			"export const findByTestAttr = (component, attr) => {",
			"  const wrapper = component.find(`[data-test='${attr}']`)",
			"  return wrapper",
			"}",
			"",
			"/**",
			"* PropTypes test",
			"* @param {ShallowWrapper} component - Component",
			"* @param {obj} expectedProps - props.",
			"* @returns {undefined} - return undefined || error ",
			"*/",
			"export const checkProps = (component, expectedProps) => {",
			"  const propsErr = checkPropTypes(component.propTypes, expectedProps, 'props', component.name);",
			"  return propsErr;",
			"}",
			"",
			"/**",
			"* test store (Redux)",
			"* @param {any} initialState - Component",
			"* @returns {any} - return store with middleware",
			"*/",
			"export const testStore = (initialState) => {",
			"  const createStoreWithMiddleware = applyMiddleware(...middlewares)(createStore);",
			"  return createStoreWithMiddleware(rootReducer, initialState);",
			"}"
		],
		"description": "z"
	},
	"z-test-setup-redux": {
		"prefix": "z-test-setup-redux",
		"body": [
			"/** ",
			"* Facroty function to create s ShallowWrapper for the App component.",
			"* @function setup",
			"* @param {object} props - Component props specific to this setup.",
			"* @param {object} state - inimial state for setup.",
			"* @returns {shallowWrapper}",
			"*/",
			"const setup = (initialState={}) => {",
			"  const store = testStore(initialState) // testStore from utils",
			"  const wrapper = shallow(<App store={store} />).childAt(0).dive() // shallow from enzyme",
			"  return wrapper",
			"}"
		],
		"description": "z"
	},
	"z-test-setup-universal": {
		"prefix": "z-test-setup-universal",
		"body": [
			"/** ",
			"* Facroty function to create s ShallowWrapper for the App component.",
			"* @function setup",
			"* @param {object} props - Component props specific to this setup.",
			"* @param {object} state - inimial state for setup.",
			"* @returns {shallowWrapper}",
			"*/",
			"const setup = (props={}, state=null) => {",
			"  const wrapper = shallow(<App {...props} />) // shallow from enzyme",
			"  if (state) wrapper.setState(state)",
			"    return wrapper",
			"}"
		],
		"description": "z-test-setup-universal"
	},
	"z-test-describe": {
		"prefix": "z-test-describe",
		"body": [
			"describe('$1', () => {",
			"  ",
			"  $2",
			"",
			"})"
		],
		"description": "z-test-describe"
	},
	"z-test-describe-before": {
		"prefix": "z-test-describe-before",
		"body": [
			"describe('$1', () => {",
			"  ",
			"  let wrapper",
			"  beforeEach(() => {",
			"    $2",
			"  })",
			"",
			"})"
		],
		"description": "z-test-describe-before"
	},
	"z-test-test": {
		"prefix": "z-test-test",
		"body": [
			"test('$1', () => {",
			"  $2",
			"})"
		],
		"description": "z-test-test"
	},
	"z-test-test-find": {
		"prefix": "z-test-test-find",
		"body": [
			"test('should render without errors', () => {",
			"  const component = findByTestAttr(wrapper, '$1')",
			"  expect(component.length).toBe(1)",
			"})"
		],
		"description": "z-test-test-find"
	},
	"z-test-integration": {
		"prefix": "z-test-integration",
		"body": [
			"import moxios from 'moxios'",
			"",
			"import { testStore } from './../../utils'",
			"import { fetchPost } from './../store/actions/posts'",
			"",
			"describe('fetchPosts action', () => {",
			"",
			"    beforeEach(() => {",
			"        moxios.install()",
			"    })",
			"",
			"    afterEach(() => {",
			"        moxios.uninstall()",
			"    })",
			"",
			"    test('Store is updated correctly', () => {",
			"",
			"        const expectedState = [{",
			"            title: 'Example title 1',",
			"            desc: 'Some Text'",
			"        },{",
			"            title: 'Example title 2',",
			"            desc: 'Some Text'",
			"        },{",
			"            title: 'Example title 3',",
			"            desc: 'Some Text'",
			"        }]",
			"        const store = testStore()",
			"",
			"        moxios.wait(() => {",
			"            const request = moxios.requests.mostRecent()",
			"            request.respondWith({",
			"                status: 200,",
			"                response: expectedState",
			"            })",
			"        })",
			"",
			"        return store.dispatch(fetchPost())",
			"        .then(() => {",
			"            const newState = store.getState()",
			"            expect(newState.reducer).toBe(expectedState)",
			"        })",
			"        ",
			"    })",
			"",
			"})"
		],
		"description": "z-test-integration"
	},
	"z-test-snapshot": {
		"prefix": "z-test-snapshot",
		"body": [
			"import renderer from 'react-test-renderer'",
			"test('snapshot renders', () => {",
			"    const component = renderer.create(<App />)",
			"    let tree = component.toJSON()",
			"    expect(tree).toMatchSnapshot()",
			"})"
		],
		"description": "z-test-snapshot"
	},
	"z-func-comp": {
		"prefix": "z-func-comp",
		"body": [
			"import React from 'react'",
			"",
			"export default function $1() {",
			"  return <div>$0</div>",
			"}"
		],
		"description": "z-func-comp"
	},
	"z-redux-ducks": {
		"prefix": "z-redux-ducks",
		"body": [
			"import { createSelector } from 'reselect'",
			"",
			"// Actions",
			"const action = {",
			"  ADD: 'ADD'",
			"}",
			"",
			"// Reducer",
			"const initialState = {",
			"  counter: 11",
			"}",
			"",
			"export default (state = initialState, { type, payload }) => {",
			"  switch (type) {",
			"",
			"  case action.ADD:",
			"    return {",
			"      ...state,",
			"      counter: state.counter + payload",
			"    }",
			"",
			"  default:",
			"    return state",
			"  }",
			"}",
			"",
			"// Action Creators",
			"export const add = num => ({",
			"  type: action.ADD,",
			"  payload: num",
			"})",
			"",
			"// side effects",
			"export const actionName = payload => dispatch => {",
			"  setTimeout(() => {",
			"    dispatch(add(payload))",
			"  }, 400)",
			"}",
			"",
			"// Selectors",
			"export const counter = createSelector(",
			"  state => state.counter.counter,",
			"  counter => counter + ' $$'",
			")"
		],
		"description": "z-redux-ducks"
	}
	// Place your snippets for javascript here. Each snippet is defined under a snippet name and has a prefix, body and 
	// description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the 
	// same ids are connected.
	// Example:
	// "Print to console": {
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
}
