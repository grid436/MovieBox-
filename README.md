# MovieBox-
Let's remove vulgarity 


patches:
  # =============================================
  # 1. PREMIUM BYPASS (Morphe Patches)
  # =============================================
  # MEMBER_CHECK_FLAGS: isPassed, getVipEnable, getVipPayEnable
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/MemberCheckResult;->isPassed()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/MemberCheckResult;->getVipEnable()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/MemberCheckResult;->getVipPayEnable()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  # MEMBER_INFO and MEMBER_BRIEF_INFO: isActive, getMemberType
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/MemberInfo;->isActive()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/MemberInfo;->getMemberType()I"
    replacement: |
      const/4 v0, 0x2  # PREMIUM_MEMBER_TYPE = 2
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/bean/MemberBriefInfo;->isActive()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/bean/MemberBriefInfo;->getMemberType()I"
    replacement: |
      const/4 v0, 0x2
      return v0

  # MEMBER_PROVIDER_FLAGS: b, g, h, B
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->b()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->g()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->h()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->B()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  # MEMBER_PROVIDER_DOWNLOAD_TASKS: D
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->D()I"
    replacement: |
      const/4 v0, 0x5  # PARALLEL_DOWNLOAD_TASKS = 5
      return v0

  # MEMBER_PROVIDER_UPSELL_DIALOG: z
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/MemberProvider;->z()V"
    replacement: |
      return-void

  # PREMIUM_PROVIDER: b, j, u, f, t, w, x, h, n
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->b()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->j()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->u()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->f()I"
    replacement: |
      const/32 v0, 0x7fffffff  # UNLIMITED = Int.MAX_VALUE
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->t()I"
    replacement: |
      const/32 v0, 0x7fffffff
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->w()I"
    replacement: |
      const/32 v0, 0x7fffffff
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->x()I"
    replacement: |
      const/32 v0, 0x7fffffff
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->h()I"
    replacement: |
      const/4 v0, 0x5  # DOWNLOAD_RESOLUTIONS = 5
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/premium/PremiumProvider;->n()I"
    replacement: |
      const/16 v0, 0x270f  # DAYS_LEFT = 9999
      return v0

  # PREMIUM_ACCESS: getHasAccess
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/memberapi/PremiumV2CheckAccessDto;->getHasAccess()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  # MEMBER_RESOLUTION: isUnlock, getVipResolutionTip
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/db/member/MemberResolutionBean;->isUnlock()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/db/member/MemberResolutionBean;->getVipResolutionTip()Z"
    replacement: |
      const/4 v0, 0x0
      return v0

  # OBSERVE_LOGIN_ACTION: onLogout
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/member/ObserveLoginAction;->onLogout()V"
    replacement: |
      return-void

  # REQUIRE_MEMBER_TYPE_HOLDERS: getRequireMemberType
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/db/download/DownloadBean;->getRequireMemberType()I"
    replacement: |
      const/4 v0, 0x0  # FREE = 0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/db/download/VipInfo;->getRequireMemberType()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/moviedetailapi/DownloadItem;->getRequireMemberType()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/shorttv/bean/DownloadItem;->getRequireMemberType()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/shorttv_pugc/bean/DownloadItem;->getRequireMemberType()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  # NEED_PAID_HOLDERS: getNeedPaid
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/shorttv/bean/ShortTVItem;->getNeedPaid()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/shorttv/bean/Subject;->getNeedPaid()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  # PLAY_MODE: b (PLAY_MODE_IS_STREAM)
  - patch_type: smali_ast_patch
    target: "Lkk/t;->b()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  # =============================================
  # 2. AD REMOVAL (Morphe Patches)
  # =============================================
  # AD_SETTINGS: c (AD_SETTINGS_ADS_OFF)
  - patch_type: smali_ast_patch
    target: "Lqi/f;->c()Z"
    replacement: |
      const/4 v0, 0x1
      return v0

  # AD_SCENE_CONFIG: t (AD_SCENE_TIMEOUT)
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/ad/scene/a;->t()I"
    replacement: |
      const/4 v0, 0x0
      return v0

  # MINTEGRAL_LOADERS: initVideo, showBanner, initNative, initInterstitial, onSplashStartLoad
  - patch_type: smali_ast_patch
    target: "Lcom/hisavana/mintegral/executer/MintegralVideo;->initVideo()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/hisavana/mintegral/executer/MintegralBanner;->showBanner()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/hisavana/mintegral/executer/MintegralNative;->initNative()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/hisavana/mintegral/executer/MintegralInterstitial;->initInterstitial()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/hisavana/mintegral/executer/MintegralSplash;->onSplashStartLoad()V"
    replacement: |
      return-void

  # =============================================
  # 3. REGION BYPASS (Morphe Patches)
  # =============================================
  # REGION_BLOCK_HANDLERS: i, j, k
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/net/AppLifeStatusInterceptor;->i()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/net/AppLifeStatusInterceptor;->j()V"
    replacement: |
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/net/AppLifeStatusInterceptor;->k()V"
    replacement: |
      return-void

  # BACKGROUND_REQUEST_FREEZE: n
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/baselib/net/AppLifeStatusInterceptor;->n()Z"
    replacement: |
      const/4 v0, 0x0
      return v0

  # =============================================
  # 4. FORCED UPDATE BYPASS (Morphe Patches)
  # =============================================
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/version/update/RemoteVersionInfo;->getForceUpdate()Z"
    replacement: |
      const/4 v0, 0x0
      return v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/version/update/RemoteVersionInfo;->getHasUpdate()Z"
    replacement: |
      const/4 v0, 0x0
      return v0

  # =============================================
  # 5. VULGARITY BLOCKING (Custom Patches)
  # =============================================
  # Inject ContentFilter to sanitize all text
  - patch_type: inject_smali_class
    class_name: "com/moviebox/ContentFilter"
    smali_code: |
      .class public Lcom/moviebox/ContentFilter;
      .super Ljava/lang/Object;

      .method public static filter(Ljava/lang/String;)Ljava/lang/String;
        .locals 5
        new-instance v0, Ljava/lang/StringBuilder;
        invoke-direct {v0}, Ljava/lang/StringBuilder;-><init>()V

        # Block adult/vulgar/anime keywords
        const-string v1, "adult"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "vulgar"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "18+"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "anime"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "hentai"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "objectification"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "mature"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "ecchi"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "nude"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "sex"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        const-string v1, "nsfw"
        invoke-virtual {p0, v1}, Ljava/lang/String;->contains(Ljava/lang/CharSequence;)Z
        move-result v1
        if-nez v1, :blocked

        # If no blocked keywords, return original
        return-object p0

        :blocked
        const-string v1, "Clean Content"
        invoke-virtual {v0, v1}, Ljava/lang/StringBuilder;->append(Ljava/lang/String;)Ljava/lang/StringBuilder;
        invoke-virtual {v0}, Ljava/lang/StringBuilder;->toString()Ljava/lang/String;
        move-result-object v0
        return-object v0
      .end method

  # Hook ContentFilter into all text-displaying methods
  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/activity/DetailActivity;->setTitle(Ljava/lang/String;)V"
    replacement: |
      .locals 3
      invoke-static {p1}, Lcom/moviebox/ContentFilter;->filter(Ljava/lang/String;)Ljava/lang/String;
      move-result-object v0
      invoke-super {p0, v0}, Landroid/app/Activity;->setTitle(Ljava/lang/CharSequence;)V
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/adapter/MovieAdapter;->onBindViewHolder(Landroidx.recyclerview.widget.RecyclerView$ViewHolder;I)V"
    replacement: |
      .locals 5
      invoke-static {p1}, Lcom/moviebox/ContentFilter;->filter(Ljava/lang/String;)Ljava/lang/String;
      move-result-object v0
      # Continue with original logic (if needed)
      return-void

  # Hook into TextView.setText (if possible)
  - patch_type: smali_ast_patch
    target: "Landroid/widget/TextView;->setText(Ljava/lang/CharSequence;)V"
    replacement: |
      .locals 3
      invoke-static {p1}, Lcom/moviebox/ContentFilter;->filter(Ljava/lang/String;)Ljava/lang/String;
      move-result-object v0
      invoke-super {p0, v0}, Landroid/widget/TextView;->setText(Ljava/lang/CharSequence;)V
      return-void

  # =============================================
  # 6. CLEAN UI (No Vulgarity or Recommendations)
  # =============================================
  # Replace vulgar strings in resources.arsc
  - patch_type: binary_resource_patch
    resource_id: 0x7f050001  # Replace with actual ID for vulgar strings
    new_value: "Clean Content"

  - patch_type: binary_resource_patch
    resource_id: 0x7f050002  # Replace with actual ID for "18+"
    new_value: "Family-Friendly"

  # Replace adult thumbnails with placeholders
  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/adapter/MovieAdapter;->loadThumbnail(Ljava/lang/String;)Landroid/graphics/Bitmap;"
    replacement: |
      .locals 3
      # Return a placeholder bitmap
      new-instance v0, Landroid/graphics/Bitmap;
      const/4 v1, 0x1  # Width
      const/4 v2, 0x1  # Height
      invoke-direct {v0, v1, v2}, Landroid/graphics/Bitmap;->createBitmap(II)Landroid/graphics/Bitmap;
      return-object v0

  # Hide recommendation sections
  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/HomeActivity;->loadRecommendations()V"
    replacement: |
      .locals 1
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/adapter/RecommendationAdapter;->onBindViewHolder(Landroidx.recyclerview.widget.RecyclerView$ViewHolder;I)V"
    replacement: |
      .locals 3
      return-void

  - patch_type: smali_ast_patch
    target: "Lcom/moviebox/ui/fragment/RecommendationFragment;->onCreateView(Landroid/view/LayoutInflater;Landroid/view/ViewGroup;Landroid/os/Bundle;)Landroid/view/View;"
    replacement: |
      .locals 5
      const/4 v0, 0x0
      return-object v0

  # =============================================
  # 7. SIM OPERATOR SPOOFING (Morphe Patches)
  # =============================================
  - patch_type: smali_ast_patch
    target: "Lcom/transsion/api/gateway/utils/DeviceUtils;->getSimOperator()Ljava/lang/String;"
    replacement: |
      const-string v0, ""
      return-object v0

  - patch_type: smali_ast_patch
    target: "Lcom/transsion/core/deviceinfo/DeviceInfo;->f()Ljava/lang/String;"
    replacement: |
      const-string v0, ""
      return-object v0

  - patch_type: smali_ast_patch
    target: "Loh/b;->o()Ljava/lang/String;"
    replacement: |
      const-string v0, ""
      return-object v0
