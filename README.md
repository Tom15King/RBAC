# RBAC
##用户test1可以查看的页面（Sys_menu）

###SELECT MenuID,MenuName from cf_privilege,sys_menu ,cf_user WHERE cf_user.LoginName="test1" and cf_privilege.PrivilegeMaster="CF_User"
###AND cf_user.UserID=cf_privilege.privilegeMasterKey 
###AND cf_privilege.PrivilegeAccess="Sys_Menu" and cf_privilege.PrivilegeAccessKey=sys_menu.MenuID and cf_privilege.PrivilegeOperation="Permit" UNION 
###SELECT MenuID,MenuName FROM cf_privilege,sys_menu ,cf_user,cf_userrole,cf_role WHERE cf_user.LoginName="test1" and cf_user.UserID=cf_userrole.UserID and cf_privilege.PrivilegeMaster="CF_Role" and cf_privilege.privilegeMasterKey=cf_role.RoleID
###AND cf_privilege.PrivilegeAccess="Sys_Menu" and cf_privilege.PrivilegeAccessKey=sys_menu.MenuID and cf_privilege.PrivilegeOperation="Permit"

<img src="" />
