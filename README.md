# hello-world

@Override
public void onInitializeAccessibilityNodeInfo(AccessibilityNodeInfo info) {
    super.onInitializeAccessibilityNodeInfo(info);
    info.setContentDescription("Graph showing sales for October");
}


View customView = new View(this);
ViewCompat.setAccessibilityDelegate(customView, new AccessibilityDelegateCompat() {
    @Override
    public void onInitializeAccessibilityNodeInfo(View host, AccessibilityNodeInfoCompat info) {
        super.onInitializeAccessibilityNodeInfo(host, info);
        info.setContentDescription("Custom dynamic view showing temperature chart");
    }
});
