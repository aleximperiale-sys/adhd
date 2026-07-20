# Before / after examples

## Explaining a bug fix

**Before:**

The issue was actually happening because the retry logic in the client was catching the timeout exception but then it was also swallowing the underlying connection error at the same time which meant that by the time it got to the point where it was supposed to log the failure and fall back to the cached value, the original error context had already been lost, so what you were seeing in the logs was just a generic "request failed" message instead of the actual root cause, and additionally there's a related issue where the cache TTL is configured in seconds in one place and milliseconds in another which compounds the confusion, though that second part isn't blocking anything right now.

**After:**

Fixed: the retry logic was swallowing the original connection error, so logs only showed "request failed" instead of the root cause.

Also noticed (not fixed yet): cache TTL is configured in seconds in one place and milliseconds in another. Want me to fix that too?

## Planning a multi-step task

**Before:**

To add the new export feature you'll need to update the API endpoint to accept a format parameter, then add a serializer for CSV output, then wire up the frontend button to call the new endpoint with the right parameter, and you'll also want to add a loading state while the export runs, plus handle the error case if the export fails, and don't forget to add a test for the new endpoint.

**After:**

Plan (6 steps):
1. Add `format` parameter to the export API endpoint
2. Add a CSV serializer
3. Wire the frontend export button to the new endpoint
4. Add a loading state during export
5. Add an error state if export fails
6. Add a test for the new endpoint

Starting with step 1.

## Reporting progress mid-task

**Before:** *(nothing said until all 6 steps are done, then one long summary)*

**After:**

Step 1 done: `format` param added to the endpoint.
Next: adding the CSV serializer (step 2).
