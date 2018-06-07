# Feature toggles

## Naming convention

The name of the toggles should follow the notation `stc-toggle-name`, where the toggle name is only alphanumeric characters plus hyphens.

## Implementation
Currently the features library is only available on the frontend and its initialised as an SDK. To use it
on your component you should use the internal state of the component to track the value, since the library
won't be available on the first render, but only after its loaded and initialised.

You can use it with your component by using react-redux to map the relevant toggle onto the components props via a connected component. There's already a generic selector available for you to use like this:

```

import { getFeature } from "template/state/modules/features"

mapStateToProps = state => ({
    gdprEnabled: getFeature(state, "stc-minibag-dropdown")
})
```

## List of toggles

| Toggle name                | Description                                                    | Default value |
| -------------------------- | -------------------------------------------------------------- | ------------- |
| `stc-minibag-dropdown`     | Activates miniBag dropdown                                     | Off           |
| `stc-welcome-mat-changes`  | Activates new Welcome Mat visibility rules & propisition info  | Off           |
| `stc-use-modern-search-url` | When turned on, simply points the search form to `/search/` rather than encode the search term in the path | Off |
| `stc-gdpr-phase-two`       | Removes the banner and activates the modal delay               | Off           |
| `stc-gdpr-deadline-copy`   | Shows GDPR deadline copy                                       | Off           |
