parentNode.appendChild(child); <- appendChildToContainer()

flushSyncCallbacks() -> callback = callback(isSync); -> commitRoot() => commitRootImpl(root, previousUpdateLanePriority); ->commitMutationEffects() -> commitMutationEffects_begin(root); -> commitMutationEffectsOnFiber(fiber, root); ->var parentFiber = getHostParentFiber(finishedWork); -> appendChildToContainer() -> parentNode.appendChild(child);
