# hello-world



AccessibilityManager am = 
    (AccessibilityManager) getSystemService(Context.ACCESSIBILITY_SERVICE);
if (am.isEnabled()) {
    AccessibilityEvent event = AccessibilityEvent.obtain(
        AccessibilityEvent.TYPE_ANNOUNCEMENT);
    event.setClassName(getClass().getName());
    event.setPackageName(getPackageName());
    event.getText().add("New content loaded in web view");
    am.sendAccessibilityEvent(event);
}
