# Changelog

## 1.0.0 (2025-12-30)


### ⚠ BREAKING CHANGES

* **useClock:** No longer provides the tick constants (DAYS, HOURS, etc), use the date-fns comparison functions.
* **useTimeout:** `timer.isActive` is now a read-only boolean instead of a getter function.
* **useInterval:** `timer.isActive` is now a read-only boolean instead of a getter function.
* **useDerivedState:** Now resets its value immediately when dependencies change, instead of waiting for next effect loop. This ensures that outgoing state is always in sync with incoming state.
* **hooks/useTimers:** This file has now been separated into its constituent imports.
* **usePageHash:** Actually returns the hash now, instead of a object.
* **usePropsMemo:** This functionality is now incorporated into useStableMemo
* **useWillUnmount:** Use useMountEffect instead.
* **useChildren:** Replaced with useMemoChildren
* Delete the root export. All hooks should be imported directly from their own imports
* Deleted all mobx hooks.
* **useAsyncCallback:** Now throws caught errors up the component tree

### removed

* **useClock:** No longer provides the tick constants (DAYS, HOURS, etc), use the date-fns comparison functions. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))


### Removed

* **hooks/useTimers:** This file has now been separated into its constituent imports. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useChildren:** Replaced with useMemoChildren ([f66a2a7](https://github.com/jimmorrison-coder/hooks/commit/f66a2a7f325472a53e199bc2fa3a32ab984f8417))
* **usePropsMemo:** This functionality is now incorporated into useStableMemo ([f66a2a7](https://github.com/jimmorrison-coder/hooks/commit/f66a2a7f325472a53e199bc2fa3a32ab984f8417))
* **useWillUnmount:** Use useMountEffect instead. ([f66a2a7](https://github.com/jimmorrison-coder/hooks/commit/f66a2a7f325472a53e199bc2fa3a32ab984f8417))


### breaking

* Delete the root export. All hooks should be imported directly from their own imports ([3ad908d](https://github.com/jimmorrison-coder/hooks/commit/3ad908d75f6a3ba28371e78e432dd682eb196b28))
* Deleted all mobx hooks. ([596f00e](https://github.com/jimmorrison-coder/hooks/commit/596f00ee9beaf24534b1d89f174468fa9e37f2f6))


### Features

* Added a base export ([c064a6f](https://github.com/jimmorrison-coder/hooks/commit/c064a6fffbbc3d112fb8a262756012f3bfd82542))
* All new typescript definitions for vscode completion. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **SelectionContext:** Context provider for managing a value selections across nested components. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **StatedContext:** Context provider for managing state across nested components. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useAsyncCallback:** New hook to handle errors coming out of an async callback function ([f344f1b](https://github.com/jimmorrison-coder/hooks/commit/f344f1bb9ced957f25da0b3b30b7ca15d387d0ae))
* **useAsyncCallback:** Now throws caught errors up the component tree ([a5fe63b](https://github.com/jimmorrison-coder/hooks/commit/a5fe63b662c3e08baaf4ba25533ef37ae15d130e))
* **useAsyncEffect:** New hook for running async effect functions ([628e5da](https://github.com/jimmorrison-coder/hooks/commit/628e5da8d3fac21056710524b3dae1c84c55c54b))
* **useChanged:** New hook for identifying when dependencies have been modified. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useChildren:** Now supports a third argument for options, with a comparison option. ([1abb59b](https://github.com/jimmorrison-coder/hooks/commit/1abb59b382b7915be524e1728f67f800d6ad4871))
* **useDebouncedEffect:** Can now accept anything for its dependencies. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useDebouncedEffect:** Now accepts a dependency comparison option on the fifth argument. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useDeferredUpdate:** New hook that generates an update callback that is guaranteed to never cause a state change during render. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useElementInViewport:** New hook to check if an element is visible within a viewport. ([27feb83](https://github.com/jimmorrison-coder/hooks/commit/27feb836fb9699ce3512308c173b72461066213d))
* **useGettableState:** Added the `defer` option to the setter function, and corrusponding `alwaysDefer` option to the hook invocation. This controls if calling the setter should immediately trigger setState, or defer to the next cycle of the event loop. Setting to true allows for writes during the render function without triggering a “State change during render” error. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useGettableState:** Added the `immedate` option to the setter function, and corrusponding `alwaysImmediate` option to the hook invocation. This controls if the state update should happen when the setter is called, or if it should wait for rerender. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useImmediateEffect:** Now accepts a dependency comparison option on the third argument. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useIntervalUpdate:** New hook for triggering a component refreshes every N milliseconds since last update. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useLocalStorage:** Now accepts a third argument for options. ([ebf86f4](https://github.com/jimmorrison-coder/hooks/commit/ebf86f465ae5035d941a329f8800955761b7207e))
* **useLocalStorage:** Now has an `isJSON` option to disable json parsing/serializing of stored values. Defaults to true. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useMemoObject:** Added options object to pass through to useStableMemo, giving means of changing comparison function ([54fdcc7](https://github.com/jimmorrison-coder/hooks/commit/54fdcc79dddf718e7c4c599e96670d76f525e862))
* **useMountEffect:** New strict-mode safe hook for executing effects only on mount and dismount. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useScrollToElement:** Smoothly tweens the page scroll until the target element is in view. ([2bd580e](https://github.com/jimmorrison-coder/hooks/commit/2bd580ee1ebf62899800d890d26d7bef748a7753))
* **useSessionStorage:** Now has an `isJSON` option to disable json parsing/serializing of stored values. Defaults to true. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useSmartEffect:** New hook. Identical to useEffect, but can use anything as a dependency and performs deep comparison of dependencies by default. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useSuspense:** New hook for performing an async task across a react suspension. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useUpdateEffect:** Can now accept anything for its dependencies. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useUpdateEffect:** Now accepts a dependency comparison option on the third argument. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useViewportIsIdle:** New hook for tracking if the user is inactive. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))


### Bug Fixes

* Bump @twipped/utils to 7.0.0 ([1da909a](https://github.com/jimmorrison-coder/hooks/commit/1da909af4638bc33cdc28f9ef3fabc5dbbb23174))
* Clean up duplicate imports ([5085fa7](https://github.com/jimmorrison-coder/hooks/commit/5085fa7ee5bfce06caef88e71cbd0a4d090d11e5))
* Corrected a whole host of broken includes. ([5149dd2](https://github.com/jimmorrison-coder/hooks/commit/5149dd2984953d482f8f596b17a7ace9e240f685))
* Fixed a whole bunch of little bugs caught by react-hooks linter ([49f46ba](https://github.com/jimmorrison-coder/hooks/commit/49f46bad743f0e640b9af7f252d79d81f6939a2c))
* Hopefully corrected typescript exports ([35bdb6c](https://github.com/jimmorrison-coder/hooks/commit/35bdb6c1c781a21b5635b6311a7b2dd7eb22f968))
* Removed the bad import from index.js ([2f5ca79](https://github.com/jimmorrison-coder/hooks/commit/2f5ca792cd93807da625446b516be74860088d5f))
* **useClock:** No longer incorrectly triggers an update immediately after first render. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useClock:** Now functions properly in StrictMode ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useComputed:** Now uses shallowEqual by default, as the docs say. ([2054707](https://github.com/jimmorrison-coder/hooks/commit/20547071e4008ba7465c0d08dc9d3166cad41940))
* **useDebounce:** Now functions properly in StrictMode ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useDefer:** Fixed a bug that would cause the timeout handle to get lost on component refresh ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useDerivedState:** Now resets its value immediately when dependencies change, instead of waiting for next effect loop. This ensures that outgoing state is always in sync with incoming state. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useGettableState:** Now supports passing a callback to the setter function, same as the native useState. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useGettableState:** The getter and setter functions will no longer change every render if the initial value is an object or array. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useInterval:** `timer.isActive` is now a read-only boolean instead of a getter function. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useInterval:** Now functions properly in StrictMode ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useLazyRef:** Fixed incorrect loading of DEFAULT from @twipped/utils ([5664e54](https://github.com/jimmorrison-coder/hooks/commit/5664e5427390544edd198def5bc7637554b1dd71))
* **useMemoObject:** Now accepts anything as a dependency. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **usePageHash:** Actually returns the hash now, instead of a object. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useStableMemo:** Now correctly detects a dependency change if `dependencies` becomes a falsy value. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useStableMemo:** Use shallowEqual for default comparison, as the docs say. ([d3d3178](https://github.com/jimmorrison-coder/hooks/commit/d3d31782fb26b05809c4b4df1e8777d4d9f60a01))
* **useTimeout:** `timer.isActive` is now a read-only boolean instead of a getter function. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useTimeout:** Fixed a bug that would cause the timeout handle to get lost on component refresh ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useTimeout:** Now functions properly in StrictMode ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useTimeout:** When the timeout function is provided on the hook instead of the `set()` function, the timeout will now always invoke the latest rendered instance of the function. Previously it would render the instance at the time set() was called. ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useToggledState:** Fixed the state just never changing from its default ([35136c6](https://github.com/jimmorrison-coder/hooks/commit/35136c6fe3a7f5e82d8e102b85e97f9125ed6fe6))
* **useUpdateEffect:** Now functions properly in StrictMode ([e7443d6](https://github.com/jimmorrison-coder/hooks/commit/e7443d6cd067960b3c70ac0f5b985bef98823c2c))
* **useWhenElementRefReady:** Now actually works! ([fce0325](https://github.com/jimmorrison-coder/hooks/commit/fce032598c7b1fb76ba3b652e1e996934e2983c8))

## [2.0.0](https://github.com/Twipped/hooks/compare/v1.1.0...v2.0.0) (2024-05-28)


### ⚠ BREAKING CHANGES

* **useClock:** No longer provides the tick constants (DAYS, HOURS, etc), use the date-fns comparison functions.
* **useTimeout:** `timer.isActive` is now a read-only boolean instead of a getter function.
* **useInterval:** `timer.isActive` is now a read-only boolean instead of a getter function.
* **useDerivedState:** Now resets its value immediately when dependencies change, instead of waiting for next effect loop. This ensures that outgoing state is always in sync with incoming state.
* **hooks/useTimers:** This file has now been separated into its constituent imports.
* **usePageHash:** Actually returns the hash now, instead of a object.
* **usePropsMemo:** This functionality is now incorporated into useStableMemo
* **useWillUnmount:** Use useMountEffect instead.
* **useChildren:** Replaced with useMemoChildren

### removed

* **useClock:** No longer provides the tick constants (DAYS, HOURS, etc), use the date-fns comparison functions. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))


### Removed

* **hooks/useTimers:** This file has now been separated into its constituent imports. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useChildren:** Replaced with useMemoChildren ([6397634](https://github.com/Twipped/hooks/commit/639763486438e7aec8d7599556361d8a1ec3a8f0))
* **usePropsMemo:** This functionality is now incorporated into useStableMemo ([6397634](https://github.com/Twipped/hooks/commit/639763486438e7aec8d7599556361d8a1ec3a8f0))
* **useWillUnmount:** Use useMountEffect instead. ([6397634](https://github.com/Twipped/hooks/commit/639763486438e7aec8d7599556361d8a1ec3a8f0))


### Features

* All new typescript definitions for vscode completion. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **SelectionContext:** Context provider for managing a value selections across nested components. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **StatedContext:** Context provider for managing state across nested components. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useChanged:** New hook for identifying when dependencies have been modified. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDebouncedEffect:** Can now accept anything for its dependencies. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDebouncedEffect:** Now accepts a dependency comparison option on the fifth argument. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDeferredUpdate:** New hook that generates an update callback that is guaranteed to never cause a state change during render. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useGettableState:** Added the `defer` option to the setter function, and corrusponding `alwaysDefer` option to the hook invocation. This controls if calling the setter should immediately trigger setState, or defer to the next cycle of the event loop. Setting to true allows for writes during the render function without triggering a “State change during render” error. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useGettableState:** Added the `immedate` option to the setter function, and corrusponding `alwaysImmediate` option to the hook invocation. This controls if the state update should happen when the setter is called, or if it should wait for rerender. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useImmediateEffect:** Now accepts a dependency comparison option on the third argument. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useIntervalUpdate:** New hook for triggering a component refreshes every N milliseconds since last update. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useLocalStorage:** Now has an `isJSON` option to disable json parsing/serializing of stored values. Defaults to true. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useMountEffect:** New strict-mode safe hook for executing effects only on mount and dismount. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useSessionStorage:** Now has an `isJSON` option to disable json parsing/serializing of stored values. Defaults to true. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useSmartEffect:** New hook. Identical to useEffect, but can use anything as a dependency and performs deep comparison of dependencies by default. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useSuspense:** New hook for performing an async task across a react suspension. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useUpdateEffect:** Can now accept anything for its dependencies. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useUpdateEffect:** Now accepts a dependency comparison option on the third argument. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useViewportIsIdle:** New hook for tracking if the user is inactive. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))


### Bug Fixes

* **useClock:** No longer incorrectly triggers an update immediately after first render. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useClock:** Now functions properly in StrictMode ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDebounce:** Now functions properly in StrictMode ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDefer:** Fixed a bug that would cause the timeout handle to get lost on component refresh ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useDerivedState:** Now resets its value immediately when dependencies change, instead of waiting for next effect loop. This ensures that outgoing state is always in sync with incoming state. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useGettableState:** Now supports passing a callback to the setter function, same as the native useState. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useGettableState:** The getter and setter functions will no longer change every render if the initial value is an object or array. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useInterval:** `timer.isActive` is now a read-only boolean instead of a getter function. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useInterval:** Now functions properly in StrictMode ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useMemoObject:** Now accepts anything as a dependency. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **usePageHash:** Actually returns the hash now, instead of a object. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useStableMemo:** Now correctly detects a dependency change if `dependencies` becomes a falsy value. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useTimeout:** `timer.isActive` is now a read-only boolean instead of a getter function. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useTimeout:** Fixed a bug that would cause the timeout handle to get lost on component refresh ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useTimeout:** Now functions properly in StrictMode ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useTimeout:** When the timeout function is provided on the hook instead of the `set()` function, the timeout will now always invoke the latest rendered instance of the function. Previously it would render the instance at the time set() was called. ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))
* **useUpdateEffect:** Now functions properly in StrictMode ([f95e96b](https://github.com/Twipped/hooks/commit/f95e96ba7e06e3ad7b027e1c74bb2e1876cb3bb9))

## [1.1.0](https://github.com/Twipped/hooks/compare/v1.0.0...v1.1.0) (2023-09-28)


### Features

* Added a base export ([4285983](https://github.com/Twipped/hooks/commit/42859839ca638eba120a9176fcb6c209edf71216))


### Bug Fixes

* Hopefully corrected typescript exports ([04eeda3](https://github.com/Twipped/hooks/commit/04eeda3f65f87efe54652eaeff6d90e340bf874f))

## [1.0.0](https://github.com/Twipped/hooks/compare/v0.6.2...v1.0.0) (2023-03-12)


### ⚠ BREAKING CHANGES

* Deleted the root export. All hooks should be imported directly from their named subpath imports
* Deleted all mobx hooks.

### New Hook!

* **useScrollToElement:** Smoothly tweens the page scroll until the target element is in view. ([7ba08e9](https://github.com/Twipped/hooks/commit/7ba08e99bad8631aad7cc9a1030d2d193573d9a4))

### Features

* **useLocalStorage:** Now accepts a third argument for options. Pass `isJSON: false` to treat the state as plain text without JSON serialization. ([1aa4a9d](https://github.com/Twipped/hooks/commit/1aa4a9db9d0e32c15e655ce4b13c2e22930a25d4))

### Bug Fixes

* **useToggledState:** Fixed the state just never changing from its default ([96be6d5](https://github.com/Twipped/hooks/commit/96be6d5ac66dac35e8898e67f4605ce7f321449a))
* **useWhenElementRefReady:** Now actually works! ([0b5202b](https://github.com/Twipped/hooks/commit/0b5202b335cfed9facd07b22526da0510a02aed1))

## [0.6.2](https://github.com/Twipped/hooks/compare/v0.6.1...v0.6.2) (2022-10-10)


### Bug Fixes

* Bump @twipped/utils to 7.0.0 ([f27aaa6](https://github.com/Twipped/hooks/commit/f27aaa6a12ea7c585e748cac7e5ecae04c0feb02))

## [0.6.1](https://github.com/Twipped/hooks/compare/v0.6.0...v0.6.1) (2022-10-10)


### Bug Fixes

* **useLazyRef:** Fixed incorrect loading of DEFAULT from @twipped/utils ([f701034](https://github.com/Twipped/hooks/commit/f70103420e80ff0220b689086e35746ac41e3275))

## [0.6.0](https://github.com/Twipped/hooks/compare/v0.5.0...v0.6.0) (2022-10-07)


### ⚠ BREAKING CHANGES

* **useAsyncCallback:** Now throws caught errors up the component tree

### Features

* **useAsyncCallback:** Now throws caught errors up the component tree ([24eb92f](https://github.com/Twipped/hooks/commit/24eb92f6484d70c9f067754eaa3fbc3273748e4b))
* **useAsyncEffect:** New hook for running async effect functions ([d40a114](https://github.com/Twipped/hooks/commit/d40a11439af2f35681463c128d9a88c41a51f1f8))


### Bug Fixes

* Clean up duplicate imports ([8e48306](https://github.com/Twipped/hooks/commit/8e483065d364e985e4141f04177d7c4c091f2613))
* Fixed a whole bunch of little bugs caught by react-hooks linter ([76986a2](https://github.com/Twipped/hooks/commit/76986a29b05da1b185ed63b06b168ff6c77ee7d2))

## [0.5.0](https://github.com/Twipped/hooks/compare/v0.4.0...v0.5.0) (2022-03-17)


### Features

* **useChildren:** Now supports a third argument for options, with a comparison option. ([8866860](https://github.com/Twipped/hooks/commit/88668606e1cb8c96b5f0214f3069078ad67d01d7))


### Bug Fixes

* Corrected a whole host of broken includes. ([251238a](https://github.com/Twipped/hooks/commit/251238a5eb8beeb3827b35b3f6c3ed40c14513dc))
* **useComputed:** Now uses shallowEqual by default, as the docs say. ([45ae67c](https://github.com/Twipped/hooks/commit/45ae67c5b96e40b4257a481afc353d2fc68bc685))

## [0.4.0](https://github.com/Twipped/hooks/compare/v0.3.1...v0.4.0) (2022-03-16)


### Bug Fixes

* Removed the bad import from index.js ([dddf0a0](https://github.com/Twipped/hooks/commit/dddf0a04ec78494a7a56b9574bc5b20a658d9078))
* **useStableMemo:** Use shallowEqual for default comparison, as the docs say. ([1a1b572](https://github.com/Twipped/hooks/commit/1a1b5726b52f04d69d4e75734766915c28bd1c6a))


### Features

* **useAsyncCallback:** New hook to handle errors coming out of an async callback function ([6028208](https://github.com/Twipped/hooks/commit/60282080b1f09a535ab88f1d905f32cc83f991f6))
* **useElementInViewport:** New hook to check if an element is visible within a viewport. ([ffcf012](https://github.com/Twipped/hooks/commit/ffcf01284886c15b25d19b19cb084a89ba9f3d15))
* **useMemoObject:** Added options object to pass through to useStableMemo, giving means of changing comparison function ([799e46a](https://github.com/Twipped/hooks/commit/799e46ab9e919164c2a870628ec382eac5670f82))

0.3.1 / 2022-02-22
==================

  * BREAKING: `useComputed` now receives an options object as a third parameter, with `comparison` as a configurable.
  * BREAKING: `useWhenElementRefReady` now uses useLayoutEffect if available and accepts a callback return to invoke when the ref changes again.
  * BREAKING: `useGettableState` no longer recognizes the `onlyUpdateOnDiff` option. This is instead inferred if alwaysUpdate is false.
  * BREAKING: `useIncrementer` now returns an array with the incrementing value, and a reset function.
  * BREAKING: `useTripWire` now returns an array with the wire status and a reset function.
  * BREAKING: `usePageFocus` now returns an array with the focus state, an alias to Window.focus(), and a getter function.
  * BREAKING: The third argument of `useSmartEffect` is now an options object containing the `comparison` key.
  * BREAKING: `useSmartEffect` now defaults to shallow equality, instead of an array comparison. Dependencies may now be an object.
  * DELETED: `useCallbackHook`    (use useState)
  * DELETED: `useIsFocusVisible`  (use @mui/utils)
  * DELETED: `useLocalObservable` (use mobx-react-lite)
  * DELETED: `usePageHashContext` (moved to @twipped/react-utils/page-hash-map)
  * DELETED: `useDerivedSet`      (use mobx, this never worked right, anyway)
  * DELETED: `useSafeState`       (Always felt redundant, and I hated the DX of it)
  * DELETED: `usePosition`        (use useComponentPosition, I somehow ended up with two of these)
  * FIX: `useEventHandlerOn` now detaches if the ref changes.
  * ADD: `useIsomorphicEffect`
  * ADD: `useProxyRef`
  * FEATURE: `useLocalStorage` and `useSessionStorage` will now delete the key from storage if the passed value is `undefined`.
  * FEATURE: `usePromisedState` now returns an error value that updates if a request fails.
  * DOCS: They exist!
  * FIX: The package now includes index.js (oops, thought it did that automatically)


0.2.0 / 2022-01-17
==================

  * Initial Release
